---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementIdentityProvider.md
ms.openlocfilehash: d2d689c9df73f7cd9bb6df6a5153e9afa71cb39d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675895"
---
# <span data-ttu-id="fbb14-101">Set-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="fbb14-101">Set-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="fbb14-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fbb14-102">SYNOPSIS</span></span>
<span data-ttu-id="fbb14-103">Aggiorna la configurazione di un provider di identità esistente.</span><span class="sxs-lookup"><span data-stu-id="fbb14-103">Updates the Configuration of an existing Identity Provider.</span></span>

## <span data-ttu-id="fbb14-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fbb14-104">SYNTAX</span></span>

### <span data-ttu-id="fbb14-105">ExpandedParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fbb14-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-ClientId <String>] [-ClientSecret <String>]
 [-AllowedTenants <String[]>] [-Authority <String>] [-SignupPolicyName <String>] [-SigninPolicyName <String>]
 [-ProfileEditingPolicyName <String>] [-PasswordResetPolicyName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fbb14-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="fbb14-106">ByInputObject</span></span>
```
Set-AzApiManagementIdentityProvider -InputObject <PsApiManagementIdentityProvider> [-ClientId <String>]
 [-ClientSecret <String>] [-AllowedTenants <String[]>] [-Authority <String>] [-SignupPolicyName <String>]
 [-SigninPolicyName <String>] [-ProfileEditingPolicyName <String>] [-PasswordResetPolicyName <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fbb14-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fbb14-107">DESCRIPTION</span></span>
<span data-ttu-id="fbb14-108">Aggiorna la configurazione di un provider di identità esistente.</span><span class="sxs-lookup"><span data-stu-id="fbb14-108">Updates the Configuration of an existing Identity Provider.</span></span>

## <span data-ttu-id="fbb14-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fbb14-109">EXAMPLES</span></span>

### <span data-ttu-id="fbb14-110">Esempio 1: aggiornare il provider di identità di Facebook</span><span class="sxs-lookup"><span data-stu-id="fbb14-110">Example 1 : Update the facebook Identity Provider</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Set-AzApiManagementIdentityProvider -Context $apimContext -Type Facebook -ClientSecret "updatedSecret" -PassThru
```

<span data-ttu-id="fbb14-111">Il cmdlet aggiorna il segreto client del provider di identità di Facebook;</span><span class="sxs-lookup"><span data-stu-id="fbb14-111">The cmdlet updates the Client Secret of the Facebook Identity Provider;</span></span>

## <span data-ttu-id="fbb14-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fbb14-112">PARAMETERS</span></span>

### <span data-ttu-id="fbb14-113">-AllowedTenants</span><span class="sxs-lookup"><span data-stu-id="fbb14-113">-AllowedTenants</span></span>
<span data-ttu-id="fbb14-114">Elenco dei tenant di Azure Active Directory consentiti.</span><span class="sxs-lookup"><span data-stu-id="fbb14-114">List of allowed Azure Active Directory Tenants.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbb14-115">-Authority</span><span class="sxs-lookup"><span data-stu-id="fbb14-115">-Authority</span></span>
<span data-ttu-id="fbb14-116">OpenID Connect Discovery endpoint hostname per AAD o AAD B2C.</span><span class="sxs-lookup"><span data-stu-id="fbb14-116">OpenID Connect discovery endpoint hostname for AAD or AAD B2C.</span></span> <span data-ttu-id="fbb14-117">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="fbb14-117">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbb14-118">-ClientID</span><span class="sxs-lookup"><span data-stu-id="fbb14-118">-ClientId</span></span>
<span data-ttu-id="fbb14-119">ID client dell'applicazione nel provider di identità esterna.</span><span class="sxs-lookup"><span data-stu-id="fbb14-119">Client Id of the Application in the external Identity Provider.</span></span>
<span data-ttu-id="fbb14-120">Si tratta di ID app per Facebook login, ID client per l'account di accesso di Google, ID app per Microsoft.</span><span class="sxs-lookup"><span data-stu-id="fbb14-120">It is App ID for Facebook login, Client ID for Google login, App ID for Microsoft.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbb14-121">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="fbb14-121">-ClientSecret</span></span>
<span data-ttu-id="fbb14-122">Segreto client dell'applicazione nel provider di identità esterna, usato per autenticare la richiesta di accesso.</span><span class="sxs-lookup"><span data-stu-id="fbb14-122">Client secret of the Application in external Identity Provider, used to authenticate login request.</span></span>
<span data-ttu-id="fbb14-123">Ad esempio, è l'app Secret per Facebook login, API Key per Google login, chiave pubblica per Microsoft.</span><span class="sxs-lookup"><span data-stu-id="fbb14-123">For example, it is App Secret for Facebook login, API Key for Google login, Public Key for Microsoft.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbb14-124">-Contesto</span><span class="sxs-lookup"><span data-stu-id="fbb14-124">-Context</span></span>
<span data-ttu-id="fbb14-125">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="fbb14-125">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="fbb14-126">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="fbb14-126">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fbb14-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbb14-127">-DefaultProfile</span></span>
<span data-ttu-id="fbb14-128">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fbb14-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbb14-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fbb14-129">-InputObject</span></span>
<span data-ttu-id="fbb14-130">Istanza di PsApiManagementIdentityProvider.</span><span class="sxs-lookup"><span data-stu-id="fbb14-130">Instance of PsApiManagementIdentityProvider.</span></span> <span data-ttu-id="fbb14-131">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="fbb14-131">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fbb14-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fbb14-132">-PassThru</span></span>
<span data-ttu-id="fbb14-133">Indica che questo cmdlet restituisce il  **PsApiManagementIdentityProvider** modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fbb14-133">Indicates that this cmdlet returns the  **PsApiManagementIdentityProvider** that this cmdlet modifies.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbb14-134">-PasswordResetPolicyName</span><span class="sxs-lookup"><span data-stu-id="fbb14-134">-PasswordResetPolicyName</span></span>
<span data-ttu-id="fbb14-135">Nome criterio reimpostare la password.</span><span class="sxs-lookup"><span data-stu-id="fbb14-135">Password Reset Policy Name.</span></span> <span data-ttu-id="fbb14-136">Si applica solo al provider di identità AAD B2C.</span><span class="sxs-lookup"><span data-stu-id="fbb14-136">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="fbb14-137">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="fbb14-137">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbb14-138">-ProfileEditingPolicyName</span><span class="sxs-lookup"><span data-stu-id="fbb14-138">-ProfileEditingPolicyName</span></span>
<span data-ttu-id="fbb14-139">Nome criterio di modifica del profilo.</span><span class="sxs-lookup"><span data-stu-id="fbb14-139">Profile Editing Policy Name.</span></span> <span data-ttu-id="fbb14-140">Si applica solo al provider di identità AAD B2C.</span><span class="sxs-lookup"><span data-stu-id="fbb14-140">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="fbb14-141">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="fbb14-141">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbb14-142">-SigninPolicyName</span><span class="sxs-lookup"><span data-stu-id="fbb14-142">-SigninPolicyName</span></span>
<span data-ttu-id="fbb14-143">Nome criterio di accesso.</span><span class="sxs-lookup"><span data-stu-id="fbb14-143">Signin Policy Name.</span></span> <span data-ttu-id="fbb14-144">Si applica solo al provider di identità AAD B2C.</span><span class="sxs-lookup"><span data-stu-id="fbb14-144">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="fbb14-145">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="fbb14-145">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbb14-146">-SignupPolicyName</span><span class="sxs-lookup"><span data-stu-id="fbb14-146">-SignupPolicyName</span></span>
<span data-ttu-id="fbb14-147">Nome del criterio di registrazione.</span><span class="sxs-lookup"><span data-stu-id="fbb14-147">Signup Policy Name.</span></span> <span data-ttu-id="fbb14-148">Si applica solo al provider di identità AAD B2C.</span><span class="sxs-lookup"><span data-stu-id="fbb14-148">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="fbb14-149">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="fbb14-149">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbb14-150">-Digitare</span><span class="sxs-lookup"><span data-stu-id="fbb14-150">-Type</span></span>
<span data-ttu-id="fbb14-151">Identificatore di un provider di identità esistente.</span><span class="sxs-lookup"><span data-stu-id="fbb14-151">Identifier of an existing Identity Provider.</span></span>
<span data-ttu-id="fbb14-152">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="fbb14-152">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType
Parameter Sets: ExpandedParameter
Aliases:
Accepted values: Facebook, Google, Microsoft, Twitter, Aad, AadB2C

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbb14-153">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fbb14-153">-Confirm</span></span>
<span data-ttu-id="fbb14-154">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fbb14-154">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbb14-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fbb14-155">-WhatIf</span></span>
<span data-ttu-id="fbb14-156">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fbb14-156">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fbb14-157">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fbb14-157">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbb14-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbb14-158">CommonParameters</span></span>
<span data-ttu-id="fbb14-159">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbb14-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbb14-160">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fbb14-160">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbb14-161">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fbb14-161">INPUTS</span></span>

### <span data-ttu-id="fbb14-162">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="fbb14-162">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="fbb14-163">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="fbb14-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

### <span data-ttu-id="fbb14-164">System. String</span><span class="sxs-lookup"><span data-stu-id="fbb14-164">System.String</span></span>

### <span data-ttu-id="fbb14-165">System. String []</span><span class="sxs-lookup"><span data-stu-id="fbb14-165">System.String[]</span></span>

### <span data-ttu-id="fbb14-166">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="fbb14-166">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="fbb14-167">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fbb14-167">OUTPUTS</span></span>

### <span data-ttu-id="fbb14-168">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="fbb14-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="fbb14-169">Note</span><span class="sxs-lookup"><span data-stu-id="fbb14-169">NOTES</span></span>

## <span data-ttu-id="fbb14-170">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fbb14-170">RELATED LINKS</span></span>

[<span data-ttu-id="fbb14-171">New-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="fbb14-171">New-AzApiManagementIdentityProvider</span></span>](./New-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="fbb14-172">Get-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="fbb14-172">Get-AzApiManagementIdentityProvider</span></span>](./Get-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="fbb14-173">Remove-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="fbb14-173">Remove-AzApiManagementIdentityProvider</span></span>](./Remove-AzApiManagementIdentityProvider.md)
