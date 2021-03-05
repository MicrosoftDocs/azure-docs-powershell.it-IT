---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: A2B4ACC1-6F53-47DE-A2D4-831E8AC89A5C
online version: https://docs.microsoft.com/powershell/module/az.cognitiveservices/new-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccount.md
ms.openlocfilehash: e6ed6669c98a54a037bcbdc579e08459cdff568e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981198"
---
# <span data-ttu-id="0a942-101">New-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="0a942-101">New-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="0a942-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a942-102">SYNOPSIS</span></span>
<span data-ttu-id="0a942-103">Crea un account di Servizi cognitivi.</span><span class="sxs-lookup"><span data-stu-id="0a942-103">Creates a Cognitive Services account.</span></span>

## <span data-ttu-id="0a942-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0a942-104">SYNTAX</span></span>

### <span data-ttu-id="0a942-105">CognitiveServicesEncryption</span><span class="sxs-lookup"><span data-stu-id="0a942-105">CognitiveServicesEncryption</span></span>
```
New-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-CustomSubdomainName <String>]
 [-AssignIdentity] [-StorageAccountId <String[]>] [-CognitiveServicesEncryption]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-PublicNetworkAccess <String>]
 [-ApiProperty <CognitiveServicesAccountApiProperties>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a942-106">KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="0a942-106">KeyVaultEncryption</span></span>
```
New-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-CustomSubdomainName <String>]
 [-AssignIdentity] [-StorageAccountId <String[]>] [-KeyVaultEncryption] -KeyName <String> -KeyVersion <String>
 -KeyVaultUri <String> [-NetworkRuleSet <PSNetworkRuleSet>] [-PublicNetworkAccess <String>]
 [-ApiProperty <CognitiveServicesAccountApiProperties>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a942-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0a942-107">DESCRIPTION</span></span>
<span data-ttu-id="0a942-108">Il cmdlet **New-AzCognitiveServicesAccount** crea un account di Servizi cognitivi con il tipo e SKU specificati.</span><span class="sxs-lookup"><span data-stu-id="0a942-108">The **New-AzCognitiveServicesAccount** cmdlet creates a Cognitive Services account with the specified type and SKU.</span></span>

## <span data-ttu-id="0a942-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0a942-109">EXAMPLES</span></span>

### <span data-ttu-id="0a942-110">1:</span><span class="sxs-lookup"><span data-stu-id="0a942-110">1:</span></span>
```
PS C:\> New-AzCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis -Type LUIS -SkuName S0 -Locatio
n 'WestUS'


ResourceGroupName : cognitive-services-resource-group
AccountName       : myluis
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/cognitive-services-resource-group/providers/Microsoft.Cog
                    nitiveServices/accounts/myluis
Endpoint          : https://westus.api.cognitive.microsoft.com/luis/v2.0
Location          : WestUS
Sku               : Microsoft.Azure.Management.CognitiveServices.Models.Sku
AccountType       : LUIS
ResourceType      : Microsoft.CognitiveServices/accounts
Etag              : "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
ProvisioningState : Succeeded
Tags              :
```

## <span data-ttu-id="0a942-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0a942-111">PARAMETERS</span></span>

### <span data-ttu-id="0a942-112">-ApiProperty</span><span class="sxs-lookup"><span data-stu-id="0a942-112">-ApiProperty</span></span>
<span data-ttu-id="0a942-113">ApiProperties dell'account di Servizi cognitivi.</span><span class="sxs-lookup"><span data-stu-id="0a942-113">The ApiProperties of Cognitive Services Account.</span></span> <span data-ttu-id="0a942-114">Obbligatorio per tipi di account specifici.</span><span class="sxs-lookup"><span data-stu-id="0a942-114">Required by specific account types.</span></span>

```yaml
Type: Microsoft.Azure.Management.CognitiveServices.Models.CognitiveServicesAccountApiProperties
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a942-115">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="0a942-115">-AssignIdentity</span></span>
<span data-ttu-id="0a942-116">Generare e assegnare una nuova identità dell'account di Servizi cognitivi per questo account di archiviazione per l'uso con servizi di gestione delle chiavi come Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="0a942-116">Generate and assign a new Cognitive Services Account Identity for this storage account for use with key management services like Azure KeyVault.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a942-117">-CognitiveServicesEncryption</span><span class="sxs-lookup"><span data-stu-id="0a942-117">-CognitiveServicesEncryption</span></span>
<span data-ttu-id="0a942-118">Se impostare o meno KeySource di crittografia dell'account dei Servizi cognitivi su Microsoft.CognitiveServices.</span><span class="sxs-lookup"><span data-stu-id="0a942-118">Whether to set Cognitive Services Account Encryption KeySource to Microsoft.CognitiveServices or not.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CognitiveServicesEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a942-119">-CustomSubdomainName</span><span class="sxs-lookup"><span data-stu-id="0a942-119">-CustomSubdomainName</span></span>
<span data-ttu-id="0a942-120">Nome sottodominio account di Servizi cognitivi.</span><span class="sxs-lookup"><span data-stu-id="0a942-120">Cognitive Services Account Subdomain Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a942-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a942-121">-DefaultProfile</span></span>
<span data-ttu-id="0a942-122">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="0a942-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0a942-123">-Force</span><span class="sxs-lookup"><span data-stu-id="0a942-123">-Force</span></span>
<span data-ttu-id="0a942-124">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="0a942-124">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a942-125">-KeyName</span><span class="sxs-lookup"><span data-stu-id="0a942-125">-KeyName</span></span>
<span data-ttu-id="0a942-126">Chiave di crittografia dell'account di Servizi cognitiviSource KeyVault KeyName</span><span class="sxs-lookup"><span data-stu-id="0a942-126">Cognitive Services Account encryption keySource KeyVault KeyName</span></span>

```yaml
Type: System.String
Parameter Sets: KeyVaultEncryption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a942-127">-KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="0a942-127">-KeyVaultEncryption</span></span>
<span data-ttu-id="0a942-128">Se impostare o meno la chiave di crittografia dell'account dei servizi cognitivi su Microsoft.KeyVault.</span><span class="sxs-lookup"><span data-stu-id="0a942-128">Whether to set Cognitive Services Account encryption keySource to Microsoft.KeyVault or not.</span></span> <span data-ttu-id="0a942-129">Se si specifica KeyName, KeyVersion e KeyVaultUri, anche Cognitive Services Account Encryption KeySource verrà impostato su Microsoft.KeyVault meteo che questo parametro è impostato o meno.</span><span class="sxs-lookup"><span data-stu-id="0a942-129">If you specify KeyName, KeyVersion and KeyVaultUri, Cognitive Services Account Encryption KeySource will also be set to Microsoft.KeyVault weather this parameter is set or not.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: KeyVaultEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a942-130">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="0a942-130">-KeyVaultUri</span></span>
<span data-ttu-id="0a942-131">Chiave di crittografia dell'account dei servizi cognitiviSource KeyVault KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="0a942-131">Cognitive Services Account encryption keySource KeyVault KeyVaultUri</span></span>

```yaml
Type: System.String
Parameter Sets: KeyVaultEncryption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a942-132">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="0a942-132">-KeyVersion</span></span>
<span data-ttu-id="0a942-133">Chiave di crittografia dell'account dei servizi cognitiviSource KeyVault KeyVersion</span><span class="sxs-lookup"><span data-stu-id="0a942-133">Cognitive Services Account encryption keySource KeyVault KeyVersion</span></span>

```yaml
Type: System.String
Parameter Sets: KeyVaultEncryption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a942-134">-Location</span><span class="sxs-lookup"><span data-stu-id="0a942-134">-Location</span></span>
<span data-ttu-id="0a942-135">Specifica la posizione in cui creare l'account.</span><span class="sxs-lookup"><span data-stu-id="0a942-135">Specifies the location in which to create the account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a942-136">-Name</span><span class="sxs-lookup"><span data-stu-id="0a942-136">-Name</span></span>
<span data-ttu-id="0a942-137">Specifica il nome dell'account.</span><span class="sxs-lookup"><span data-stu-id="0a942-137">Specifies the name for the account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a942-138">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="0a942-138">-NetworkRuleSet</span></span>
<span data-ttu-id="0a942-139">NetworkRuleSet viene usato per definire un set di regole di configurazione per firewall e reti virtuali, oltre che per impostare valori per le proprietà di rete, ad esempio come gestire le richieste che non corrispondono a nessuna delle regole definite</span><span class="sxs-lookup"><span data-stu-id="0a942-139">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as how to handle requests that don't match any of the defined rules</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSNetworkRuleSet
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a942-140">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="0a942-140">-PublicNetworkAccess</span></span>
<span data-ttu-id="0a942-141">Tipo di accesso di rete per l'account di Servizi cognitivi.</span><span class="sxs-lookup"><span data-stu-id="0a942-141">The network access type for Cognitive Services Account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a942-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a942-142">-ResourceGroupName</span></span>
<span data-ttu-id="0a942-143">Specifica il nome del gruppo di risorse a cui assegnare l'account.</span><span class="sxs-lookup"><span data-stu-id="0a942-143">Specifies the name of the resource group to which to assign the account.</span></span>
<span data-ttu-id="0a942-144">Il gruppo di risorse deve essere già esistente.</span><span class="sxs-lookup"><span data-stu-id="0a942-144">The resource group must already exist.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a942-145">-SKUName</span><span class="sxs-lookup"><span data-stu-id="0a942-145">-SkuName</span></span>
<span data-ttu-id="0a942-146">Specifica lo SKU per l'account.</span><span class="sxs-lookup"><span data-stu-id="0a942-146">Specifies the SKU for the account.</span></span>
<span data-ttu-id="0a942-147">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="0a942-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0a942-148">F0 (livello gratuito)</span><span class="sxs-lookup"><span data-stu-id="0a942-148">F0 (free tier)</span></span>
- <span data-ttu-id="0a942-149">S0</span><span class="sxs-lookup"><span data-stu-id="0a942-149">S0</span></span>
- <span data-ttu-id="0a942-150">S1</span><span class="sxs-lookup"><span data-stu-id="0a942-150">S1</span></span>
- <span data-ttu-id="0a942-151">S2</span><span class="sxs-lookup"><span data-stu-id="0a942-151">S2</span></span>
- <span data-ttu-id="0a942-152">S3</span><span class="sxs-lookup"><span data-stu-id="0a942-152">S3</span></span>
- <span data-ttu-id="0a942-153">S4 Per altre informazioni, vedere LE [API dei servizi cognitivi.](https://www.microsoft.com/cognitive-services/en-us/apis)</span><span class="sxs-lookup"><span data-stu-id="0a942-153">S4 For more information, see [Cognitive Service APIs](https://www.microsoft.com/cognitive-services/en-us/apis).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a942-154">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="0a942-154">-StorageAccountId</span></span>
<span data-ttu-id="0a942-155">Elenco degli account di archiviazione di proprietà dell'utente.</span><span class="sxs-lookup"><span data-stu-id="0a942-155">List of User Owned Storage Accounts.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a942-156">-Tag</span><span class="sxs-lookup"><span data-stu-id="0a942-156">-Tag</span></span>
<span data-ttu-id="0a942-157">Specifica un tag come coppia nome/valore.</span><span class="sxs-lookup"><span data-stu-id="0a942-157">Specifies a tag as a name/value pair.</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a942-158">-Type</span><span class="sxs-lookup"><span data-stu-id="0a942-158">-Type</span></span>
<span data-ttu-id="0a942-159">Specifica il tipo di account da creare.</span><span class="sxs-lookup"><span data-stu-id="0a942-159">Specifies the type of account to create.</span></span> <span data-ttu-id="0a942-160">Usare `Get-AzCognitiveServicesAccountType` il cmdlet per ottenere i valori accettabili correnti.</span><span class="sxs-lookup"><span data-stu-id="0a942-160">Use `Get-AzCognitiveServicesAccountType` cmdlet to get current acceptable values.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountType, AccountType, Kind

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a942-161">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0a942-161">-Confirm</span></span>
<span data-ttu-id="0a942-162">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0a942-162">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a942-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a942-163">-WhatIf</span></span>
<span data-ttu-id="0a942-164">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0a942-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a942-165">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0a942-165">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a942-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a942-166">CommonParameters</span></span>
<span data-ttu-id="0a942-167">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a942-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a942-168">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0a942-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a942-169">INPUT</span><span class="sxs-lookup"><span data-stu-id="0a942-169">INPUTS</span></span>

### <span data-ttu-id="0a942-170">System.String</span><span class="sxs-lookup"><span data-stu-id="0a942-170">System.String</span></span>

## <span data-ttu-id="0a942-171">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0a942-171">OUTPUTS</span></span>

### <span data-ttu-id="0a942-172">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="0a942-172">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="0a942-173">NOTE</span><span class="sxs-lookup"><span data-stu-id="0a942-173">NOTES</span></span>

## <span data-ttu-id="0a942-174">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0a942-174">RELATED LINKS</span></span>

[<span data-ttu-id="0a942-175">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="0a942-175">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="0a942-176">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="0a942-176">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)

[<span data-ttu-id="0a942-177">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="0a942-177">Set-AzCognitiveServicesAccount</span></span>](./Set-AzCognitiveServicesAccount.md)
