---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: F58FD77E-2946-44B1-B410-6E983FC20E21
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADApplication.md
ms.openlocfilehash: e23e3db6cb574fb16b2c559c948372c808840de1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514840"
---
# <span data-ttu-id="fd76c-101">New-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="fd76c-101">New-AzureRmADApplication</span></span>

## <span data-ttu-id="fd76c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fd76c-102">SYNOPSIS</span></span>
<span data-ttu-id="fd76c-103">Crea una nuova applicazione di Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="fd76c-103">Creates a new azure active directory application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd76c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fd76c-104">SYNTAX</span></span>

### <span data-ttu-id="fd76c-105">ApplicationWithoutCredentialParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fd76c-105">ApplicationWithoutCredentialParameterSet (Default)</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd76c-106">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd76c-106">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd76c-107">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd76c-107">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -PasswordCredentials <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd76c-108">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd76c-108">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd76c-109">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd76c-109">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -KeyCredentials <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd76c-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fd76c-110">DESCRIPTION</span></span>
<span data-ttu-id="fd76c-111">Crea una nuova applicazione di Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="fd76c-111">Creates a new azure active directory application.</span></span>

## <span data-ttu-id="fd76c-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fd76c-112">EXAMPLES</span></span>

### <span data-ttu-id="fd76c-113">Esempio 1-creare una nuova applicazione AAD.</span><span class="sxs-lookup"><span data-stu-id="fd76c-113">Example 1 - Create new AAD application.</span></span>

```
PS C:\> New-AzureRmADApplication -DisplayName "NewApplication" -HomePage "https://www.microsoft.com" -IdentifierUris "http://NewApplication"
```

<span data-ttu-id="fd76c-114">Crea una nuova applicazione di Azure Active Directory senza credenziali.</span><span class="sxs-lookup"><span data-stu-id="fd76c-114">Creates a new azure active directory application without any credentials.</span></span>

### <span data-ttu-id="fd76c-115">Esempio 2: creare una nuova applicazione AAD con la password.</span><span class="sxs-lookup"><span data-stu-id="fd76c-115">Example 2 - Create new AAD application with password.</span></span>

```
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> New-AzureRmADApplication -DisplayName "NewApplication" -HomePage "https://www.microsoft.com" -IdentifierUris "http:
//NewApplication" -Password $SecureStringPassword
```

<span data-ttu-id="fd76c-116">Crea una nuova applicazione di Azure Active Directory e associa le credenziali di password.</span><span class="sxs-lookup"><span data-stu-id="fd76c-116">Creates a new azure active directory application and associates password credentials with it.</span></span>

## <span data-ttu-id="fd76c-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fd76c-117">PARAMETERS</span></span>

### <span data-ttu-id="fd76c-118">-AvailableToOtherTenants</span><span class="sxs-lookup"><span data-stu-id="fd76c-118">-AvailableToOtherTenants</span></span>
<span data-ttu-id="fd76c-119">Valore che specifica se l'applicazione è un singolo tenant o un multi-tenant.</span><span class="sxs-lookup"><span data-stu-id="fd76c-119">The value specifying whether the application is a single tenant or a multi-tenant.</span></span>

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

### <span data-ttu-id="fd76c-120">-CertValue</span><span class="sxs-lookup"><span data-stu-id="fd76c-120">-CertValue</span></span>
<span data-ttu-id="fd76c-121">Il valore del tipo di credenziale "asimmetrico".</span><span class="sxs-lookup"><span data-stu-id="fd76c-121">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="fd76c-122">Rappresenta il certificato codificato 64 di base.</span><span class="sxs-lookup"><span data-stu-id="fd76c-122">It represents the base 64 encoded certificate.</span></span>

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

### <span data-ttu-id="fd76c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd76c-123">-DefaultProfile</span></span>
<span data-ttu-id="fd76c-124">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="fd76c-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd76c-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="fd76c-125">-DisplayName</span></span>
<span data-ttu-id="fd76c-126">Nome visualizzato della nuova applicazione.</span><span class="sxs-lookup"><span data-stu-id="fd76c-126">Display name of the new application.</span></span>

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

### <span data-ttu-id="fd76c-127">-EndDate</span><span class="sxs-lookup"><span data-stu-id="fd76c-127">-EndDate</span></span>
<span data-ttu-id="fd76c-128">Data di fine effettiva dell'utilizzo delle credenziali.</span><span class="sxs-lookup"><span data-stu-id="fd76c-128">The effective end date of the credential usage.</span></span>
<span data-ttu-id="fd76c-129">Il valore di data di fine predefinito è di un anno da oggi.</span><span class="sxs-lookup"><span data-stu-id="fd76c-129">The default end date value is one year from today.</span></span> <span data-ttu-id="fd76c-130">Per le credenziali di tipo "asimmetrico", deve essere impostato su attivato o prima della data in cui il certificato X509 è valido.</span><span class="sxs-lookup"><span data-stu-id="fd76c-130">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="fd76c-131">-Home page</span><span class="sxs-lookup"><span data-stu-id="fd76c-131">-HomePage</span></span>
<span data-ttu-id="fd76c-132">URL della Home page dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="fd76c-132">The URL to the application homepage.</span></span>

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

### <span data-ttu-id="fd76c-133">-IdentifierUris</span><span class="sxs-lookup"><span data-stu-id="fd76c-133">-IdentifierUris</span></span>
<span data-ttu-id="fd76c-134">URI che identificano l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="fd76c-134">The URIs that identify the application.</span></span>

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

### <span data-ttu-id="fd76c-135">-Credenziali di i</span><span class="sxs-lookup"><span data-stu-id="fd76c-135">-KeyCredentials</span></span>
<span data-ttu-id="fd76c-136">Elenco delle credenziali di certificato associate all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="fd76c-136">The list of certificate credentials associated with the application.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd76c-137">-Password</span><span class="sxs-lookup"><span data-stu-id="fd76c-137">-Password</span></span>
<span data-ttu-id="fd76c-138">La password da associare all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="fd76c-138">The password to be associated with the application.</span></span>

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

### <span data-ttu-id="fd76c-139">-PasswordCredentials</span><span class="sxs-lookup"><span data-stu-id="fd76c-139">-PasswordCredentials</span></span>
<span data-ttu-id="fd76c-140">Elenco delle credenziali di password associate all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="fd76c-140">The list of password credentials associated with the application.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationWithPasswordCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd76c-141">-ReplyUrls</span><span class="sxs-lookup"><span data-stu-id="fd76c-141">-ReplyUrls</span></span>
<span data-ttu-id="fd76c-142">URL di risposta dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="fd76c-142">The application reply urls.</span></span>

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

### <span data-ttu-id="fd76c-143">-StartDate</span><span class="sxs-lookup"><span data-stu-id="fd76c-143">-StartDate</span></span>
<span data-ttu-id="fd76c-144">Data di inizio effettiva dell'utilizzo delle credenziali.</span><span class="sxs-lookup"><span data-stu-id="fd76c-144">The effective start date of the credential usage.</span></span>
<span data-ttu-id="fd76c-145">Il valore predefinito della data di inizio è oggi.</span><span class="sxs-lookup"><span data-stu-id="fd76c-145">The default start date value is today.</span></span> <span data-ttu-id="fd76c-146">Per le credenziali di tipo "asimmetrico", deve essere impostato su attivato o successivo alla data di validità del certificato X509.</span><span class="sxs-lookup"><span data-stu-id="fd76c-146">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="fd76c-147">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fd76c-147">-Confirm</span></span>
<span data-ttu-id="fd76c-148">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd76c-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd76c-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd76c-149">-WhatIf</span></span>
<span data-ttu-id="fd76c-150">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fd76c-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd76c-151">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fd76c-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd76c-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd76c-152">CommonParameters</span></span>
<span data-ttu-id="fd76c-153">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd76c-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd76c-154">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd76c-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd76c-155">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fd76c-155">INPUTS</span></span>

### <span data-ttu-id="fd76c-156">System. String</span><span class="sxs-lookup"><span data-stu-id="fd76c-156">System.String</span></span>

### <span data-ttu-id="fd76c-157">System. String []</span><span class="sxs-lookup"><span data-stu-id="fd76c-157">System.String[]</span></span>

### <span data-ttu-id="fd76c-158">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fd76c-158">System.Boolean</span></span>

### <span data-ttu-id="fd76c-159">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADPasswordCredential []</span><span class="sxs-lookup"><span data-stu-id="fd76c-159">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADPasswordCredential[]</span></span>

### <span data-ttu-id="fd76c-160">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADKeyCredential []</span><span class="sxs-lookup"><span data-stu-id="fd76c-160">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADKeyCredential[]</span></span>

### <span data-ttu-id="fd76c-161">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="fd76c-161">System.Security.SecureString</span></span>

### <span data-ttu-id="fd76c-162">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="fd76c-162">System.DateTime</span></span>

## <span data-ttu-id="fd76c-163">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fd76c-163">OUTPUTS</span></span>

### <span data-ttu-id="fd76c-164">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="fd76c-164">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="fd76c-165">Note</span><span class="sxs-lookup"><span data-stu-id="fd76c-165">NOTES</span></span>
<span data-ttu-id="fd76c-166">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Resource, Group, template, Deployment</span><span class="sxs-lookup"><span data-stu-id="fd76c-166">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="fd76c-167">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fd76c-167">RELATED LINKS</span></span>

[<span data-ttu-id="fd76c-168">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="fd76c-168">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="fd76c-169">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="fd76c-169">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

[<span data-ttu-id="fd76c-170">New-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="fd76c-170">New-AzureRmADServicePrincipal</span></span>](./New-AzureRmADServicePrincipal.md)

[<span data-ttu-id="fd76c-171">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="fd76c-171">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="fd76c-172">New-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="fd76c-172">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="fd76c-173">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="fd76c-173">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

