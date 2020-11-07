---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: F58FD77E-2946-44B1-B410-6E983FC20E21
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermadapplication
schema: 2.0.0
ms.openlocfilehash: 71e5e6c3cc80235b68df5c90e95a96e760abf80b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866633"
---
# <span data-ttu-id="4b04b-101">New-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="4b04b-101">New-AzureRmADApplication</span></span>

## <span data-ttu-id="4b04b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4b04b-102">SYNOPSIS</span></span>
<span data-ttu-id="4b04b-103">Crea una nuova applicazione di Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="4b04b-103">Creates a new azure active directory application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4b04b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4b04b-104">SYNTAX</span></span>

### <span data-ttu-id="4b04b-105">ApplicationWithoutCredentialParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4b04b-105">ApplicationWithoutCredentialParameterSet (Default)</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b04b-106">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="4b04b-106">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b04b-107">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="4b04b-107">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -PasswordCredentials <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b04b-108">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="4b04b-108">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b04b-109">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="4b04b-109">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -KeyCredentials <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b04b-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4b04b-110">DESCRIPTION</span></span>
<span data-ttu-id="4b04b-111">Crea una nuova applicazione di Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="4b04b-111">Creates a new azure active directory application.</span></span>

## <span data-ttu-id="4b04b-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4b04b-112">EXAMPLES</span></span>

### <span data-ttu-id="4b04b-113">Esempio 1-creare una nuova applicazione AAD.</span><span class="sxs-lookup"><span data-stu-id="4b04b-113">Example 1 - Create new AAD application.</span></span>

```
PS C:\> New-AzureRmADApplication -DisplayName "NewApplication" -HomePage "https://www.microsoft.com" -IdentifierUris "http://NewApplication"
```

<span data-ttu-id="4b04b-114">Crea una nuova applicazione di Azure Active Directory senza credenziali.</span><span class="sxs-lookup"><span data-stu-id="4b04b-114">Creates a new azure active directory application without any credentials.</span></span>

### <span data-ttu-id="4b04b-115">Esempio 2: creare una nuova applicazione AAD con la password.</span><span class="sxs-lookup"><span data-stu-id="4b04b-115">Example 2 - Create new AAD application with password.</span></span>

```
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> New-AzureRmADApplication -DisplayName "NewApplication" -HomePage "https://www.microsoft.com" -IdentifierUris "http:
//NewApplication" -Password $SecureStringPassword
```

<span data-ttu-id="4b04b-116">Crea una nuova applicazione di Azure Active Directory e associa le credenziali di password.</span><span class="sxs-lookup"><span data-stu-id="4b04b-116">Creates a new azure active directory application and associates password credentials with it.</span></span>

## <span data-ttu-id="4b04b-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4b04b-117">PARAMETERS</span></span>

### <span data-ttu-id="4b04b-118">-AvailableToOtherTenants</span><span class="sxs-lookup"><span data-stu-id="4b04b-118">-AvailableToOtherTenants</span></span>
<span data-ttu-id="4b04b-119">Valore che specifica se l'applicazione è un singolo tenant o un multi-tenant.</span><span class="sxs-lookup"><span data-stu-id="4b04b-119">The value specifying whether the application is a single tenant or a multi-tenant.</span></span>

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

### <span data-ttu-id="4b04b-120">-CertValue</span><span class="sxs-lookup"><span data-stu-id="4b04b-120">-CertValue</span></span>
<span data-ttu-id="4b04b-121">Il valore del tipo di credenziale "asimmetrico".</span><span class="sxs-lookup"><span data-stu-id="4b04b-121">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="4b04b-122">Rappresenta il certificato codificato 64 di base.</span><span class="sxs-lookup"><span data-stu-id="4b04b-122">It represents the base 64 encoded certificate.</span></span>

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

### <span data-ttu-id="4b04b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b04b-123">-DefaultProfile</span></span>
<span data-ttu-id="4b04b-124">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="4b04b-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4b04b-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="4b04b-125">-DisplayName</span></span>
<span data-ttu-id="4b04b-126">Nome visualizzato della nuova applicazione.</span><span class="sxs-lookup"><span data-stu-id="4b04b-126">Display name of the new application.</span></span>

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

### <span data-ttu-id="4b04b-127">-EndDate</span><span class="sxs-lookup"><span data-stu-id="4b04b-127">-EndDate</span></span>
<span data-ttu-id="4b04b-128">Data di fine effettiva dell'utilizzo delle credenziali.</span><span class="sxs-lookup"><span data-stu-id="4b04b-128">The effective end date of the credential usage.</span></span>
<span data-ttu-id="4b04b-129">Il valore di data di fine predefinito è di un anno da oggi.</span><span class="sxs-lookup"><span data-stu-id="4b04b-129">The default end date value is one year from today.</span></span> <span data-ttu-id="4b04b-130">Per le credenziali di tipo "asimmetrico", deve essere impostato su attivato o prima della data in cui il certificato X509 è valido.</span><span class="sxs-lookup"><span data-stu-id="4b04b-130">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="4b04b-131">-Home page</span><span class="sxs-lookup"><span data-stu-id="4b04b-131">-HomePage</span></span>
<span data-ttu-id="4b04b-132">URL della Home page dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4b04b-132">The URL to the application homepage.</span></span>

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

### <span data-ttu-id="4b04b-133">-IdentifierUris</span><span class="sxs-lookup"><span data-stu-id="4b04b-133">-IdentifierUris</span></span>
<span data-ttu-id="4b04b-134">URI che identificano l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4b04b-134">The URIs that identify the application.</span></span>

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

### <span data-ttu-id="4b04b-135">-Credenziali di i</span><span class="sxs-lookup"><span data-stu-id="4b04b-135">-KeyCredentials</span></span>
<span data-ttu-id="4b04b-136">Elenco delle credenziali di certificato associate all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4b04b-136">The list of certificate credentials associated with the application.</span></span>

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

### <span data-ttu-id="4b04b-137">-Password</span><span class="sxs-lookup"><span data-stu-id="4b04b-137">-Password</span></span>
<span data-ttu-id="4b04b-138">La password da associare all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4b04b-138">The password to be associated with the application.</span></span>

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

### <span data-ttu-id="4b04b-139">-PasswordCredentials</span><span class="sxs-lookup"><span data-stu-id="4b04b-139">-PasswordCredentials</span></span>
<span data-ttu-id="4b04b-140">Elenco delle credenziali di password associate all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4b04b-140">The list of password credentials associated with the application.</span></span>

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

### <span data-ttu-id="4b04b-141">-ReplyUrls</span><span class="sxs-lookup"><span data-stu-id="4b04b-141">-ReplyUrls</span></span>
<span data-ttu-id="4b04b-142">URL di risposta dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4b04b-142">The application reply urls.</span></span>

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

### <span data-ttu-id="4b04b-143">-StartDate</span><span class="sxs-lookup"><span data-stu-id="4b04b-143">-StartDate</span></span>
<span data-ttu-id="4b04b-144">Data di inizio effettiva dell'utilizzo delle credenziali.</span><span class="sxs-lookup"><span data-stu-id="4b04b-144">The effective start date of the credential usage.</span></span>
<span data-ttu-id="4b04b-145">Il valore predefinito della data di inizio è oggi.</span><span class="sxs-lookup"><span data-stu-id="4b04b-145">The default start date value is today.</span></span> <span data-ttu-id="4b04b-146">Per le credenziali di tipo "asimmetrico", deve essere impostato su attivato o successivo alla data di validità del certificato X509.</span><span class="sxs-lookup"><span data-stu-id="4b04b-146">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="4b04b-147">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4b04b-147">-Confirm</span></span>
<span data-ttu-id="4b04b-148">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4b04b-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b04b-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b04b-149">-WhatIf</span></span>
<span data-ttu-id="4b04b-150">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4b04b-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b04b-151">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4b04b-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b04b-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b04b-152">CommonParameters</span></span>
<span data-ttu-id="4b04b-153">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b04b-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b04b-154">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b04b-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b04b-155">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4b04b-155">INPUTS</span></span>

### <span data-ttu-id="4b04b-156">System. String</span><span class="sxs-lookup"><span data-stu-id="4b04b-156">System.String</span></span>

### <span data-ttu-id="4b04b-157">System. String []</span><span class="sxs-lookup"><span data-stu-id="4b04b-157">System.String[]</span></span>

### <span data-ttu-id="4b04b-158">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4b04b-158">System.Boolean</span></span>

### <span data-ttu-id="4b04b-159">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADPasswordCredential []</span><span class="sxs-lookup"><span data-stu-id="4b04b-159">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADPasswordCredential[]</span></span>

### <span data-ttu-id="4b04b-160">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADKeyCredential []</span><span class="sxs-lookup"><span data-stu-id="4b04b-160">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADKeyCredential[]</span></span>

### <span data-ttu-id="4b04b-161">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="4b04b-161">System.Security.SecureString</span></span>

### <span data-ttu-id="4b04b-162">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="4b04b-162">System.DateTime</span></span>

## <span data-ttu-id="4b04b-163">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4b04b-163">OUTPUTS</span></span>

### <span data-ttu-id="4b04b-164">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="4b04b-164">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="4b04b-165">Note</span><span class="sxs-lookup"><span data-stu-id="4b04b-165">NOTES</span></span>
<span data-ttu-id="4b04b-166">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Resource, Group, template, Deployment</span><span class="sxs-lookup"><span data-stu-id="4b04b-166">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="4b04b-167">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4b04b-167">RELATED LINKS</span></span>

[<span data-ttu-id="4b04b-168">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="4b04b-168">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="4b04b-169">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="4b04b-169">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

[<span data-ttu-id="4b04b-170">New-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="4b04b-170">New-AzureRmADServicePrincipal</span></span>](./New-AzureRmADServicePrincipal.md)

[<span data-ttu-id="4b04b-171">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="4b04b-171">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="4b04b-172">New-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="4b04b-172">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="4b04b-173">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="4b04b-173">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

