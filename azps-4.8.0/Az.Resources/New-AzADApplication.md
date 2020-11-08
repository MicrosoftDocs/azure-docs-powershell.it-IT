---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: F58FD77E-2946-44B1-B410-6E983FC20E21
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADApplication.md
ms.openlocfilehash: 7ab7c679bc623a9eaa0f99bcdba1ab8281bd7d8f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188933"
---
# <span data-ttu-id="e91cc-101">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="e91cc-101">New-AzADApplication</span></span>

## <span data-ttu-id="e91cc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e91cc-102">SYNOPSIS</span></span>
<span data-ttu-id="e91cc-103">Crea una nuova applicazione di Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e91cc-103">Creates a new azure active directory application.</span></span>

## <span data-ttu-id="e91cc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e91cc-104">SYNTAX</span></span>

### <span data-ttu-id="e91cc-105">ApplicationWithoutCredentialParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e91cc-105">ApplicationWithoutCredentialParameterSet (Default)</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e91cc-106">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="e91cc-106">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e91cc-107">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="e91cc-107">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -PasswordCredentials <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e91cc-108">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="e91cc-108">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e91cc-109">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="e91cc-109">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -KeyCredentials <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e91cc-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e91cc-110">DESCRIPTION</span></span>
<span data-ttu-id="e91cc-111">Crea una nuova applicazione di Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e91cc-111">Creates a new azure active directory application.</span></span> <span data-ttu-id="e91cc-112">Di seguito sono elencate le autorizzazioni necessarie per creare un'applicazione:</span><span class="sxs-lookup"><span data-stu-id="e91cc-112">Below are the permissions needed to create an application:</span></span>

- <span data-ttu-id="e91cc-113">Grafico di Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="e91cc-113">Azure Active Directory Graph</span></span>
  - <span data-ttu-id="e91cc-114">Application. ReadWrite. OwnedBy</span><span class="sxs-lookup"><span data-stu-id="e91cc-114">Application.ReadWrite.OwnedBy</span></span>
- <span data-ttu-id="e91cc-115">Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="e91cc-115">Microsoft Graph</span></span>
  - <span data-ttu-id="e91cc-116">Directory. AccessAsUser. All</span><span class="sxs-lookup"><span data-stu-id="e91cc-116">Directory.AccessAsUser.All</span></span>
  - <span data-ttu-id="e91cc-117">Directory. ReadWrite. All</span><span class="sxs-lookup"><span data-stu-id="e91cc-117">Directory.ReadWrite.All</span></span>

## <span data-ttu-id="e91cc-118">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e91cc-118">EXAMPLES</span></span>

### <span data-ttu-id="e91cc-119">Esempio 1: creare una nuova applicazione AAD.</span><span class="sxs-lookup"><span data-stu-id="e91cc-119">Example 1: Create new AAD application.</span></span>

```powershell
PS C:\> New-AzADApplication -DisplayName "NewApplication" -HomePage "http://www.microsoft.com" -IdentifierUris "http://NewApplication"
```

<span data-ttu-id="e91cc-120">Crea una nuova applicazione di Azure Active Directory senza credenziali.</span><span class="sxs-lookup"><span data-stu-id="e91cc-120">Creates a new azure active directory application without any credentials.</span></span>

### <span data-ttu-id="e91cc-121">Esempio 2: creare una nuova applicazione AAD con la password.</span><span class="sxs-lookup"><span data-stu-id="e91cc-121">Example 2: Create new AAD application with password.</span></span>

```powershell
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> New-AzADApplication -DisplayName "NewApplication" -HomePage "http://www.microsoft.com" -IdentifierUris "http:
//NewApplication" -Password $SecureStringPassword
```

<span data-ttu-id="e91cc-122">Crea una nuova applicazione di Azure Active Directory e associa le credenziali di password.</span><span class="sxs-lookup"><span data-stu-id="e91cc-122">Creates a new azure active directory application and associates password credentials with it.</span></span>

## <span data-ttu-id="e91cc-123">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e91cc-123">PARAMETERS</span></span>

### <span data-ttu-id="e91cc-124">-AvailableToOtherTenants</span><span class="sxs-lookup"><span data-stu-id="e91cc-124">-AvailableToOtherTenants</span></span>
<span data-ttu-id="e91cc-125">Valore che specifica se l'applicazione è un singolo tenant o un multi-tenant.</span><span class="sxs-lookup"><span data-stu-id="e91cc-125">The value specifying whether the application is a single tenant or a multi-tenant.</span></span>

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

### <span data-ttu-id="e91cc-126">-CertValue</span><span class="sxs-lookup"><span data-stu-id="e91cc-126">-CertValue</span></span>
<span data-ttu-id="e91cc-127">Il valore del tipo di credenziale "asimmetrico".</span><span class="sxs-lookup"><span data-stu-id="e91cc-127">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="e91cc-128">Rappresenta il certificato codificato 64 di base.</span><span class="sxs-lookup"><span data-stu-id="e91cc-128">It represents the base 64 encoded certificate.</span></span>

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

### <span data-ttu-id="e91cc-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e91cc-129">-DefaultProfile</span></span>
<span data-ttu-id="e91cc-130">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="e91cc-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e91cc-131">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="e91cc-131">-DisplayName</span></span>
<span data-ttu-id="e91cc-132">Nome visualizzato della nuova applicazione.</span><span class="sxs-lookup"><span data-stu-id="e91cc-132">Display name of the new application.</span></span>

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

### <span data-ttu-id="e91cc-133">-EndDate</span><span class="sxs-lookup"><span data-stu-id="e91cc-133">-EndDate</span></span>
<span data-ttu-id="e91cc-134">Data di fine effettiva dell'utilizzo delle credenziali.</span><span class="sxs-lookup"><span data-stu-id="e91cc-134">The effective end date of the credential usage.</span></span>
<span data-ttu-id="e91cc-135">Il valore di data di fine predefinito è di un anno da oggi.</span><span class="sxs-lookup"><span data-stu-id="e91cc-135">The default end date value is one year from today.</span></span> <span data-ttu-id="e91cc-136">Per le credenziali di tipo "asimmetrico", deve essere impostato su attivato o prima della data in cui il certificato X509 è valido.</span><span class="sxs-lookup"><span data-stu-id="e91cc-136">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="e91cc-137">-Home page</span><span class="sxs-lookup"><span data-stu-id="e91cc-137">-HomePage</span></span>
<span data-ttu-id="e91cc-138">URL della Home page dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e91cc-138">The URL to the application homepage.</span></span>

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

### <span data-ttu-id="e91cc-139">-IdentifierUris</span><span class="sxs-lookup"><span data-stu-id="e91cc-139">-IdentifierUris</span></span>
<span data-ttu-id="e91cc-140">URI che identificano l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e91cc-140">The URIs that identify the application.</span></span>

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

### <span data-ttu-id="e91cc-141">-Credenziali di i</span><span class="sxs-lookup"><span data-stu-id="e91cc-141">-KeyCredentials</span></span>
<span data-ttu-id="e91cc-142">Elenco delle credenziali di certificato associate all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e91cc-142">The list of certificate credentials associated with the application.</span></span>

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

### <span data-ttu-id="e91cc-143">-Password</span><span class="sxs-lookup"><span data-stu-id="e91cc-143">-Password</span></span>
<span data-ttu-id="e91cc-144">La password da associare all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e91cc-144">The password to be associated with the application.</span></span>

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

### <span data-ttu-id="e91cc-145">-PasswordCredentials</span><span class="sxs-lookup"><span data-stu-id="e91cc-145">-PasswordCredentials</span></span>
<span data-ttu-id="e91cc-146">Elenco delle credenziali di password associate all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e91cc-146">The list of password credentials associated with the application.</span></span>

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

### <span data-ttu-id="e91cc-147">-ReplyUrls</span><span class="sxs-lookup"><span data-stu-id="e91cc-147">-ReplyUrls</span></span>
<span data-ttu-id="e91cc-148">URL di risposta dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e91cc-148">The application reply urls.</span></span>

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

### <span data-ttu-id="e91cc-149">-StartDate</span><span class="sxs-lookup"><span data-stu-id="e91cc-149">-StartDate</span></span>
<span data-ttu-id="e91cc-150">Data di inizio effettiva dell'utilizzo delle credenziali.</span><span class="sxs-lookup"><span data-stu-id="e91cc-150">The effective start date of the credential usage.</span></span>
<span data-ttu-id="e91cc-151">Il valore predefinito della data di inizio è oggi.</span><span class="sxs-lookup"><span data-stu-id="e91cc-151">The default start date value is today.</span></span> <span data-ttu-id="e91cc-152">Per le credenziali di tipo "asimmetrico", deve essere impostato su attivato o successivo alla data di validità del certificato X509.</span><span class="sxs-lookup"><span data-stu-id="e91cc-152">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="e91cc-153">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e91cc-153">-Confirm</span></span>
<span data-ttu-id="e91cc-154">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e91cc-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e91cc-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e91cc-155">-WhatIf</span></span>
<span data-ttu-id="e91cc-156">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e91cc-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e91cc-157">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e91cc-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e91cc-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e91cc-158">CommonParameters</span></span>
<span data-ttu-id="e91cc-159">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e91cc-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e91cc-160">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e91cc-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e91cc-161">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e91cc-161">INPUTS</span></span>

### <span data-ttu-id="e91cc-162">System. String</span><span class="sxs-lookup"><span data-stu-id="e91cc-162">System.String</span></span>

### <span data-ttu-id="e91cc-163">System. String []</span><span class="sxs-lookup"><span data-stu-id="e91cc-163">System.String[]</span></span>

### <span data-ttu-id="e91cc-164">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e91cc-164">System.Boolean</span></span>

### <span data-ttu-id="e91cc-165">Microsoft. Azure. Commands. ActiveDirectory. PSADPasswordCredential []</span><span class="sxs-lookup"><span data-stu-id="e91cc-165">Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]</span></span>

### <span data-ttu-id="e91cc-166">Microsoft. Azure. Commands. ActiveDirectory. PSADKeyCredential []</span><span class="sxs-lookup"><span data-stu-id="e91cc-166">Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]</span></span>

### <span data-ttu-id="e91cc-167">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="e91cc-167">System.Security.SecureString</span></span>

### <span data-ttu-id="e91cc-168">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="e91cc-168">System.DateTime</span></span>

## <span data-ttu-id="e91cc-169">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e91cc-169">OUTPUTS</span></span>

### <span data-ttu-id="e91cc-170">Microsoft. Azure. Commands. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="e91cc-170">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="e91cc-171">Note</span><span class="sxs-lookup"><span data-stu-id="e91cc-171">NOTES</span></span>
<span data-ttu-id="e91cc-172">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Resource, Group, template, Deployment</span><span class="sxs-lookup"><span data-stu-id="e91cc-172">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="e91cc-173">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e91cc-173">RELATED LINKS</span></span>

[<span data-ttu-id="e91cc-174">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="e91cc-174">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="e91cc-175">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="e91cc-175">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

[<span data-ttu-id="e91cc-176">New-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="e91cc-176">New-AzADServicePrincipal</span></span>](./New-AzADServicePrincipal.md)

[<span data-ttu-id="e91cc-177">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="e91cc-177">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="e91cc-178">New-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="e91cc-178">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="e91cc-179">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="e91cc-179">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

