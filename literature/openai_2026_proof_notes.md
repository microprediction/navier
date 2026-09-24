# Notes on OpenAI (2026), *Finite Time Blowup for Navier–Stokes*

Distilled from Sections 1–3 and 10 of the manuscript (166 pp.) on 24 September 2026.
Page numbers refer to the released PDF.

## Theorem 1.1 (p. 1)
For every ν > 0 there exist f ∈ C_c^∞(R³ × (0,∞); R³), a compact K ⊂ R³, and smooth
(u, p) on R³ × [0,1) with ∂_t u + (u·∇)u − νΔu + ∇p = f, ∇·u = 0, u(·,0) = 0,
supp u(·,t) ∪ supp p(·,t) ⊂ K, sup_{t<1} ‖u(t)‖_{L²} < ∞, limsup_{t↑1} ‖u(t)‖_{L∞} = ∞.
Hence no global smooth bounded-energy solution with the same data. Alternative (C);
(D) via Corollary 10.6 by periodization of compactly supported fields.

## Scales (Sec. 2.1, 3.1)
τ = 1 − t, 0 < h < 1/100, A = 1/2 + h, D = 1/2 − h.
Similarity coordinates: τ = q(1 − η²), z = q^D η, X = r²/(2q); q ≍ τ on compacts away from η = ±1.
Leading field: u_θ = q^{−A} E(X,η), u_z = q^{−A} U(X,η), r u_r = V_0, p = q^{−2A} Π,
Π(X,η) = −∫_X^∞ E²/(2x) dx.
ℓ_r ≍ τ^{1/2}, ℓ_z ≍ τ^{1/2−h}; |u_θ|,|u_z| ≍ τ^{−1/2−h}; |u_r| = O(τ^{−1/2}).
Core volume τ^{3/2−h}; energy τ^{1/2−3h} → 0; dissipation rate τ^{−1/2−3h}, integrable.
Re_θ ≍ τ^{−h} → ∞; Re_r = O(1). Axial/radial diffusion ratio τ^{2h} = expansion parameter.
Growth line (3.6)/(10.21): u_θ(√(2X_in τ), 0, 0, 1−τ) = τ^{−A}(e_0 + O(τ^{2h})).

## Structure (Sec. 2–3)
1. Inner core: axisymmetric, inflow + swirl spin-up + axial outflow, slight z-asymmetry
   (nonzero u_z at z = 0) so amplification is available at every height.
2. Heat exterior: pure swirl K(r,τ) e_θ solving −∂_τ K = K_rr + K_r/r − K/r², K = r^{−1−2h} H_ext(τ/r²);
   residual zero; smooth limits at τ = 0 for every r > 0.
3. Annulus X_a < X < X_b: background residual = −div of a stress T = (T_rθ, T_rz), scale q^{−3/2−h},
   singular. Five radial moment conditions make T vanish inside and outside.
4. Pulses: localized oscillatory waves w = curl A_wave, amplitude q^{−1/2−h/2}, wavelength q^{1/2+h/2};
   ⟨w_r w_θ⟩, ⟨w_r w_z⟩ = T + h.o.t. Two families; admissible stress cone condition (T = c₁v₁ + c₂v₂,
   c_i > 0). Amplitude ODE (7.5)/(7.17): z' = (diag(λ,−λ) + E) z − d z, λ = λ₀/√(1+s²),
   d_ref = εk²B_s²(1+s²), s(v) linear in v; envelope P(v) Gaussian, P(0) exponentially small.
   Energy budget (7.22): pulse gains from shear via its own momentum flux, loses to viscosity.
   Auxiliary torus Y ∈ T² separates pulses with overlapping physical supports.
5. Correction cycle (Prop. 9.6): waves, signed stress increments, mean flow, five moments;
   σ_j = 1/5 + j/10; residual bounded by q^{hσ_j − K_m}.
6. Summation with shrinking cutoffs on potentials → flat residual: |∂^α_x ∂^b_t R| ≤ C q^N ∀N.
7. Localization (Prop. 10.1), force extension through t = 1 (Lemma 10.3, Borel-type in time),
   energy bound ‖u‖² + 2∫‖∇u‖² ≤ F(t)² (Lemma 10.4), comparison/uniqueness on [0,T], T < 1
   (Lemma 10.5), viscosity rescaling u_ν = √ν u(x/√ν, t) (10.22).

## Residual identity (Sec. 3.3)
R(u_B + w, p_B + π) = R(u_B, p_B) + L_{u_B}(w, π) + ∇·(w ⊗ w),
L_{u_B}(w,π) = ∂_t w + (u_B·∇)w + (w·∇)u_B − Δw + ∇π.

## Responses recorded
- Constantin–Ignatova–Vicol arXiv:2609.20803: analytic force + the construction's bounds ⇒ regular.
- Cao–Chi–Nie arXiv:2609.10262: blow-up forces dense in L¹_t H^s_x, s < 1/2.
- Duraiswami arXiv:2609.17642: GD1998 porous-wall swirl vs. the core; mechanism not reachable.
- Agresti arXiv:2607.15140 (v4, 9 Sep 2026): transport noise ⇒ global smooth w.h.p., Remark 4.4 for smooth f.
