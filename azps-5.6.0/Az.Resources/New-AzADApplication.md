---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: F58FD77E-2946-44B1-B410-6E983FC20E21
online version: https://docs.microsoft.com/powershell/module/az.resources/new-azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADApplication.md
ms.openlocfilehash: c2b3ebfafc1e5e11cbed69fce0cb935cf48131be
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985598"
---
# <span data-ttu-id="d525c-101">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="d525c-101">New-AzADApplication</span></span>

## <span data-ttu-id="d525c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d525c-102">SYNOPSIS</span></span>
<span data-ttu-id="d525c-103">Crea una nuova applicazione azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d525c-103">Creates a new azure active directory application.</span></span>

## <span data-ttu-id="d525c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d525c-104">SYNTAX</span></span>

### <span data-ttu-id="d525c-105">ApplicationWithoutCredentialParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d525c-105">ApplicationWithoutCredentialParameterSet (Default)</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d525c-106">ApplicationWithPasswordPparamParameterSet</span><span class="sxs-lookup"><span data-stu-id="d525c-106">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d525c-107">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="d525c-107">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -PasswordCredentials <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d525c-108">ApplicationWithKeyPparamParameterSet</span><span class="sxs-lookup"><span data-stu-id="d525c-108">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d525c-109">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="d525c-109">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -KeyCredentials <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d525c-110">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d525c-110">DESCRIPTION</span></span>
<span data-ttu-id="d525c-111">Crea una nuova applicazione azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d525c-111">Creates a new azure active directory application.</span></span> <span data-ttu-id="d525c-112">Di seguito sono elencate le autorizzazioni necessarie per creare un'applicazione:</span><span class="sxs-lookup"><span data-stu-id="d525c-112">Below are the permissions needed to create an application:</span></span>

- <span data-ttu-id="d525c-113">Azure Active Directory Graph</span><span class="sxs-lookup"><span data-stu-id="d525c-113">Azure Active Directory Graph</span></span>
  - <span data-ttu-id="d525c-114">Application.ReadWrite.OwnedBy</span><span class="sxs-lookup"><span data-stu-id="d525c-114">Application.ReadWrite.OwnedBy</span></span>
- <span data-ttu-id="d525c-115">Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="d525c-115">Microsoft Graph</span></span>
  - <span data-ttu-id="d525c-116">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="d525c-116">Directory.AccessAsUser.All</span></span>
  - <span data-ttu-id="d525c-117">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d525c-117">Directory.ReadWrite.All</span></span>

## <span data-ttu-id="d525c-118">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d525c-118">EXAMPLES</span></span>

### <span data-ttu-id="d525c-119">Esempio 1: Creare una nuova applicazione AAD.</span><span class="sxs-lookup"><span data-stu-id="d525c-119">Example 1: Create new AAD application.</span></span>

```powershell
PS C:\> New-AzADApplication -DisplayName "NewApplication" -HomePage "http://www.microsoft.com" -IdentifierUris "http://NewApplication"
```

<span data-ttu-id="d525c-120">Crea una nuova applicazione azure Active Directory senza credenziali.</span><span class="sxs-lookup"><span data-stu-id="d525c-120">Creates a new azure active directory application without any credentials.</span></span>

### <span data-ttu-id="d525c-121">Esempio 2: Creare una nuova applicazione AAD con una password.</span><span class="sxs-lookup"><span data-stu-id="d525c-121">Example 2: Create new AAD application with password.</span></span>

```powershell
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> New-AzADApplication -DisplayName "NewApplication" -HomePage "http://www.microsoft.com" -IdentifierUris "http:
//NewApplication" -Password $SecureStringPassword
```

<span data-ttu-id="d525c-122">Crea una nuova applicazione azure Active Directory e le associa le credenziali della password.</span><span class="sxs-lookup"><span data-stu-id="d525c-122">Creates a new azure active directory application and associates password credentials with it.</span></span>

## <span data-ttu-id="d525c-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d525c-123">PARAMETERS</span></span>

### <span data-ttu-id="d525c-124">-AvailableToOtherTenants</span><span class="sxs-lookup"><span data-stu-id="d525c-124">-AvailableToOtherTenants</span></span>
<span data-ttu-id="d525c-125">Valore che specifica se l'applicazione è un singolo tenant o un multi-tenant.</span><span class="sxs-lookup"><span data-stu-id="d525c-125">The value specifying whether the application is a single tenant or a multi-tenant.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d525c-126">-CertValue</span><span class="sxs-lookup"><span data-stu-id="d525c-126">-CertValue</span></span>
<span data-ttu-id="d525c-127">Valore del tipo di credenziali "asimmetrico".</span><span class="sxs-lookup"><span data-stu-id="d525c-127">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="d525c-128">Rappresenta il certificato codificato base 64.</span><span class="sxs-lookup"><span data-stu-id="d525c-128">It represents the base 64 encoded certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationWithKeyPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d525c-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d525c-129">-DefaultProfile</span></span>
<span data-ttu-id="d525c-130">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="d525c-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d525c-131">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="d525c-131">-DisplayName</span></span>
<span data-ttu-id="d525c-132">Nome visualizzato della nuova applicazione.</span><span class="sxs-lookup"><span data-stu-id="d525c-132">Display name of the new application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d525c-133">-EndDate</span><span class="sxs-lookup"><span data-stu-id="d525c-133">-EndDate</span></span>
<span data-ttu-id="d525c-134">Data di fine effettiva dell'utilizzo delle credenziali.</span><span class="sxs-lookup"><span data-stu-id="d525c-134">The effective end date of the credential usage.</span></span>
<span data-ttu-id="d525c-135">Il valore predefinito per la data di fine è a un anno dalla data odierna.</span><span class="sxs-lookup"><span data-stu-id="d525c-135">The default end date value is one year from today.</span></span> <span data-ttu-id="d525c-136">Per le credenziali di tipo "asimmetrico", questa deve essere impostata su o prima della data in cui il certificato X509 è valido.</span><span class="sxs-lookup"><span data-stu-id="d525c-136">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d525c-137">-HomePage</span><span class="sxs-lookup"><span data-stu-id="d525c-137">-HomePage</span></span>
<span data-ttu-id="d525c-138">URL della home page dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d525c-138">The URL to the application homepage.</span></span>

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

### <span data-ttu-id="d525c-139">-IdentifierUris</span><span class="sxs-lookup"><span data-stu-id="d525c-139">-IdentifierUris</span></span>
<span data-ttu-id="d525c-140">URI che identificano l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d525c-140">The URIs that identify the application.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d525c-141">-KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="d525c-141">-KeyCredentials</span></span>
<span data-ttu-id="d525c-142">Elenco delle credenziali di certificato associate all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d525c-142">The list of certificate credentials associated with the application.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d525c-143">-Password</span><span class="sxs-lookup"><span data-stu-id="d525c-143">-Password</span></span>
<span data-ttu-id="d525c-144">La password da associare all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d525c-144">The password to be associated with the application.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ApplicationWithPasswordPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d525c-145">-PasswordCredentials</span><span class="sxs-lookup"><span data-stu-id="d525c-145">-PasswordCredentials</span></span>
<span data-ttu-id="d525c-146">Elenco delle credenziali password associate all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d525c-146">The list of password credentials associated with the application.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationWithPasswordCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d525c-147">-ReplyUrls</span><span class="sxs-lookup"><span data-stu-id="d525c-147">-ReplyUrls</span></span>
<span data-ttu-id="d525c-148">URL di risposta dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d525c-148">The application reply urls.</span></span>

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

### <span data-ttu-id="d525c-149">-StartDate</span><span class="sxs-lookup"><span data-stu-id="d525c-149">-StartDate</span></span>
<span data-ttu-id="d525c-150">Data di inizio effettivo dell'utilizzo delle credenziali.</span><span class="sxs-lookup"><span data-stu-id="d525c-150">The effective start date of the credential usage.</span></span>
<span data-ttu-id="d525c-151">Il valore predefinito per la data di inizio è oggi.</span><span class="sxs-lookup"><span data-stu-id="d525c-151">The default start date value is today.</span></span> <span data-ttu-id="d525c-152">Per le credenziali di tipo "asimmetrico", questa deve essere impostata su o dopo la data da cui il certificato X509 è valido.</span><span class="sxs-lookup"><span data-stu-id="d525c-152">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d525c-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d525c-153">-Confirm</span></span>
<span data-ttu-id="d525c-154">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d525c-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d525c-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d525c-155">-WhatIf</span></span>
<span data-ttu-id="d525c-156">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d525c-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d525c-157">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d525c-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d525c-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d525c-158">CommonParameters</span></span>
<span data-ttu-id="d525c-159">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d525c-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d525c-160">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d525c-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d525c-161">INPUT</span><span class="sxs-lookup"><span data-stu-id="d525c-161">INPUTS</span></span>

### <span data-ttu-id="d525c-162">System.String</span><span class="sxs-lookup"><span data-stu-id="d525c-162">System.String</span></span>

### <span data-ttu-id="d525c-163">System.String[]</span><span class="sxs-lookup"><span data-stu-id="d525c-163">System.String[]</span></span>

### <span data-ttu-id="d525c-164">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d525c-164">System.Boolean</span></span>

### <span data-ttu-id="d525c-165">Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]</span><span class="sxs-lookup"><span data-stu-id="d525c-165">Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]</span></span>

### <span data-ttu-id="d525c-166">Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]</span><span class="sxs-lookup"><span data-stu-id="d525c-166">Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]</span></span>

### <span data-ttu-id="d525c-167">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="d525c-167">System.Security.SecureString</span></span>

### <span data-ttu-id="d525c-168">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="d525c-168">System.DateTime</span></span>

## <span data-ttu-id="d525c-169">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d525c-169">OUTPUTS</span></span>

### <span data-ttu-id="d525c-170">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="d525c-170">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="d525c-171">NOTE</span><span class="sxs-lookup"><span data-stu-id="d525c-171">NOTES</span></span>
<span data-ttu-id="d525c-172">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, risorsa, gruppo, modello, distribuzione</span><span class="sxs-lookup"><span data-stu-id="d525c-172">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="d525c-173">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d525c-173">RELATED LINKS</span></span>

[<span data-ttu-id="d525c-174">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="d525c-174">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="d525c-175">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="d525c-175">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

[<span data-ttu-id="d525c-176">New-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="d525c-176">New-AzADServicePrincipal</span></span>](./New-AzADServicePrincipal.md)

[<span data-ttu-id="d525c-177">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="d525c-177">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="d525c-178">New-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="d525c-178">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="d525c-179">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="d525c-179">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

