---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: D602F910-B26F-473D-B5B6-C7BDFB0A14CB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADServicePrincipal.md
ms.openlocfilehash: ca338fd648010b9158a6bc308bb4dcb2f1c48317
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519369"
---
# <span data-ttu-id="4f3fb-101">New-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="4f3fb-101">New-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="4f3fb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4f3fb-102">SYNOPSIS</span></span>
<span data-ttu-id="4f3fb-103">Crea una nuova entità servizio di Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="4f3fb-103">Creates a new azure active directory service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4f3fb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4f3fb-104">SYNTAX</span></span>

### <span data-ttu-id="4f3fb-105">ApplicationWithoutCredentialParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4f3fb-105">ApplicationWithoutCredentialParameterSet (Default)</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f3fb-106">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="4f3fb-106">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f3fb-107">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="4f3fb-107">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -PasswordCredentials <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f3fb-108">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="4f3fb-108">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f3fb-109">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="4f3fb-109">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -KeyCredentials <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f3fb-110">DisplayNameWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="4f3fb-110">DisplayNameWithoutCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f3fb-111">DisplayNameWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="4f3fb-111">DisplayNameWithPasswordPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f3fb-112">DisplayNameWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="4f3fb-112">DisplayNameWithPasswordCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -PasswordCredentials <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f3fb-113">DisplayNameWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="4f3fb-113">DisplayNameWithKeyPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f3fb-114">DisplayNameWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="4f3fb-114">DisplayNameWithKeyCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -KeyCredentials <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f3fb-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4f3fb-115">DESCRIPTION</span></span>
<span data-ttu-id="4f3fb-116">Crea una nuova entità servizio di Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="4f3fb-116">Creates a new azure active directory service principal.</span></span>

<span data-ttu-id="4f3fb-117">Nota: il cmdlet crea anche in modo implicito un'applicazione e ne imposta le proprietà (se il ApplicationId non è disponibile).</span><span class="sxs-lookup"><span data-stu-id="4f3fb-117">Note: The cmdlet also implicitly creates an application and sets its properties (if the ApplicationId is not provided).</span></span>
<span data-ttu-id="4f3fb-118">Per aggiornare i parametri specifici dell'applicazione, usare Set-AzureRmADApplication cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4f3fb-118">In order to update the application specific parameters please use Set-AzureRmADApplication cmdlet.</span></span>

## <span data-ttu-id="4f3fb-119">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4f3fb-119">EXAMPLES</span></span>

### <span data-ttu-id="4f3fb-120">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4f3fb-120">Example 1</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId 34a28ad2-dec4-4a41-bc3b-d22ddf90000e
```

<span data-ttu-id="4f3fb-121">Crea una nuova entità servizio di Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="4f3fb-121">Creates a new azure active directory service principal.</span></span>

<span data-ttu-id="4f3fb-122">DisplayName tipo ObjectId</span><span class="sxs-lookup"><span data-stu-id="4f3fb-122">DisplayName                    Type                           ObjectId</span></span>
-----------                    ----                           --------
<span data-ttu-id="4f3fb-123">DemoApp ServicePrincipal f95b6f5c-FC98-4af0-bb8a-34a14ca1dca1</span><span class="sxs-lookup"><span data-stu-id="4f3fb-123">DemoApp                        ServicePrincipal               f95b6f5c-fc98-4af0-bb8a-34a14ca1dca1</span></span>

### <span data-ttu-id="4f3fb-124">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="4f3fb-124">Example 2</span></span>
```
$SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
New-AzureRmADServicePrincipal -DisplayName SPForNoExistingApp -Password $SecureStringPassword
```

<span data-ttu-id="4f3fb-125">Crea una nuova entità servizio.</span><span class="sxs-lookup"><span data-stu-id="4f3fb-125">Creates a new service principal.</span></span>
<span data-ttu-id="4f3fb-126">Il cmdlet crea inoltre in modo implicito un'applicazione poiché non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="4f3fb-126">The cmdlet also implicitly creates an application since one is not provided.</span></span>

<span data-ttu-id="4f3fb-127">DisplayName tipo ObjectId</span><span class="sxs-lookup"><span data-stu-id="4f3fb-127">DisplayName                    Type                           ObjectId</span></span>
-----------                    ----                           --------
<span data-ttu-id="4f3fb-128">SPForNoExistingApp ServicePrincipal 784136ca-3ae2-4fdd-a388-89d993e7c780</span><span class="sxs-lookup"><span data-stu-id="4f3fb-128">SPForNoExistingApp             ServicePrincipal               784136ca-3ae2-4fdd-a388-89d993e7c780</span></span>

## <span data-ttu-id="4f3fb-129">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4f3fb-129">PARAMETERS</span></span>

### <span data-ttu-id="4f3fb-130">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="4f3fb-130">-ApplicationId</span></span>
<span data-ttu-id="4f3fb-131">ID applicazione univoco per un'entità di servizio in un tenant.</span><span class="sxs-lookup"><span data-stu-id="4f3fb-131">The unique application id for a service principal in a tenant.</span></span>
<span data-ttu-id="4f3fb-132">Una volta creata questa proprietà non può essere modificata.</span><span class="sxs-lookup"><span data-stu-id="4f3fb-132">Once created this property cannot be changed.</span></span>
<span data-ttu-id="4f3fb-133">Se non viene specificato un ID applicazione, verrà generato uno.</span><span class="sxs-lookup"><span data-stu-id="4f3fb-133">If an application id is not specified, one will be generated.</span></span>

```yaml
Type: Guid
Parameter Sets: ApplicationWithoutCredentialParameterSet, ApplicationWithPasswordPlainParameterSet, ApplicationWithPasswordCredentialParameterSet, ApplicationWithKeyPlainParameterSet, ApplicationWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f3fb-134">-CertValue</span><span class="sxs-lookup"><span data-stu-id="4f3fb-134">-CertValue</span></span>
<span data-ttu-id="4f3fb-135">Il valore del tipo di credenziale "asimmetrico".</span><span class="sxs-lookup"><span data-stu-id="4f3fb-135">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="4f3fb-136">Rappresenta il certificato codificato 64 di base.</span><span class="sxs-lookup"><span data-stu-id="4f3fb-136">It represents the base 64 encoded certificate.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationWithKeyPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f3fb-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f3fb-137">-DefaultProfile</span></span>
<span data-ttu-id="4f3fb-138">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="4f3fb-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f3fb-139">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="4f3fb-139">-DisplayName</span></span>
<span data-ttu-id="4f3fb-140">Nome descrittivo dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="4f3fb-140">The friendly name of the service principal.</span></span>

```yaml
Type: String
Parameter Sets: DisplayNameWithoutCredentialParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithPasswordCredentialParameterSet, DisplayNameWithKeyPlainParameterSet, DisplayNameWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f3fb-141">-EndDate</span><span class="sxs-lookup"><span data-stu-id="4f3fb-141">-EndDate</span></span>
<span data-ttu-id="4f3fb-142">Data di fine effettiva dell'utilizzo delle credenziali.</span><span class="sxs-lookup"><span data-stu-id="4f3fb-142">The effective end date of the credential usage.</span></span>
<span data-ttu-id="4f3fb-143">Il valore di data di fine predefinito è di un anno da oggi.</span><span class="sxs-lookup"><span data-stu-id="4f3fb-143">The default end date value is one year from today.</span></span> <span data-ttu-id="4f3fb-144">Per le credenziali di tipo "asimmetrico", deve essere impostato su attivato o prima della data in cui il certificato X509 è valido.</span><span class="sxs-lookup"><span data-stu-id="4f3fb-144">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f3fb-145">-Credenziali di i</span><span class="sxs-lookup"><span data-stu-id="4f3fb-145">-KeyCredentials</span></span>
<span data-ttu-id="4f3fb-146">Elenco delle credenziali di certificato associate all'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="4f3fb-146">The list of certificate credentials associated with the service principal.</span></span>

```yaml
Type: PSADKeyCredential[]
Parameter Sets: ApplicationWithKeyCredentialParameterSet, DisplayNameWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f3fb-147">-Password</span><span class="sxs-lookup"><span data-stu-id="4f3fb-147">-Password</span></span>
<span data-ttu-id="4f3fb-148">La password da associare all'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="4f3fb-148">The password to be associated with the service principal.</span></span>

```yaml
Type: SecureString
Parameter Sets: ApplicationWithPasswordPlainParameterSet, DisplayNameWithPasswordPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f3fb-149">-PasswordCredentials</span><span class="sxs-lookup"><span data-stu-id="4f3fb-149">-PasswordCredentials</span></span>
<span data-ttu-id="4f3fb-150">Elenco delle credenziali delle password associate all'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="4f3fb-150">The list of password credentials associated with the service principal.</span></span>

```yaml
Type: PSADPasswordCredential[]
Parameter Sets: ApplicationWithPasswordCredentialParameterSet, DisplayNameWithPasswordCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f3fb-151">-StartDate</span><span class="sxs-lookup"><span data-stu-id="4f3fb-151">-StartDate</span></span>
<span data-ttu-id="4f3fb-152">Data di inizio effettiva dell'utilizzo delle credenziali.</span><span class="sxs-lookup"><span data-stu-id="4f3fb-152">The effective start date of the credential usage.</span></span>
<span data-ttu-id="4f3fb-153">Il valore predefinito della data di inizio è oggi.</span><span class="sxs-lookup"><span data-stu-id="4f3fb-153">The default start date value is today.</span></span> <span data-ttu-id="4f3fb-154">Per le credenziali di tipo "asimmetrico", deve essere impostato su attivato o successivo alla data di validità del certificato X509.</span><span class="sxs-lookup"><span data-stu-id="4f3fb-154">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

```yaml
Type: DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f3fb-155">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4f3fb-155">-Confirm</span></span>
<span data-ttu-id="4f3fb-156">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4f3fb-156">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f3fb-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f3fb-157">-WhatIf</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f3fb-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f3fb-158">CommonParameters</span></span>
<span data-ttu-id="4f3fb-159">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f3fb-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f3fb-160">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f3fb-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f3fb-161">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4f3fb-161">INPUTS</span></span>

### <span data-ttu-id="4f3fb-162">Nessuno</span><span class="sxs-lookup"><span data-stu-id="4f3fb-162">None</span></span>
<span data-ttu-id="4f3fb-163">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="4f3fb-163">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4f3fb-164">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4f3fb-164">OUTPUTS</span></span>

### <span data-ttu-id="4f3fb-165">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="4f3fb-165">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="4f3fb-166">Note</span><span class="sxs-lookup"><span data-stu-id="4f3fb-166">NOTES</span></span>
<span data-ttu-id="4f3fb-167">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Resource, Group, template, Deployment</span><span class="sxs-lookup"><span data-stu-id="4f3fb-167">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="4f3fb-168">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4f3fb-168">RELATED LINKS</span></span>

[<span data-ttu-id="4f3fb-169">Remove-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="4f3fb-169">Remove-AzureRmADServicePrincipal</span></span>](./Remove-AzureRmADServicePrincipal.md)

[<span data-ttu-id="4f3fb-170">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="4f3fb-170">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

[<span data-ttu-id="4f3fb-171">New-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="4f3fb-171">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)

[<span data-ttu-id="4f3fb-172">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="4f3fb-172">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="4f3fb-173">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="4f3fb-173">Get-AzureRmADSpCredential</span></span>](./Get-AzureRmADSpCredential.md)

[<span data-ttu-id="4f3fb-174">New-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="4f3fb-174">New-AzureRmADSpCredential</span></span>](./New-AzureRmADSpCredential.md)

[<span data-ttu-id="4f3fb-175">Remove-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="4f3fb-175">Remove-AzureRmADSpCredential</span></span>](./Remove-AzureRmADSpCredential.md)

