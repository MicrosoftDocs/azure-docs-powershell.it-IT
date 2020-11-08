---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: A2B4ACC1-6F53-47DE-A2D4-831E8AC89A5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/new-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccount.md
ms.openlocfilehash: 713c5cb34133a233bace576ea80035b8e004eb7f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94018271"
---
# <span data-ttu-id="0c6f0-101">New-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="0c6f0-101">New-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="0c6f0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0c6f0-102">SYNOPSIS</span></span>
<span data-ttu-id="0c6f0-103">Crea un account di servizi cognitivi.</span><span class="sxs-lookup"><span data-stu-id="0c6f0-103">Creates a Cognitive Services account.</span></span>

## <span data-ttu-id="0c6f0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0c6f0-104">SYNTAX</span></span>

### <span data-ttu-id="0c6f0-105">CognitiveServicesEncryption</span><span class="sxs-lookup"><span data-stu-id="0c6f0-105">CognitiveServicesEncryption</span></span>
```
New-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-CustomSubdomainName <String>]
 [-AssignIdentity] [-StorageAccountId <String[]>] [-CognitiveServicesEncryption]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0c6f0-106">KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="0c6f0-106">KeyVaultEncryption</span></span>
```
New-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-CustomSubdomainName <String>]
 [-AssignIdentity] [-StorageAccountId <String[]>] [-KeyVaultEncryption] -KeyName <String> -KeyVersion <String>
 -KeyVaultUri <String> [-NetworkRuleSet <PSNetworkRuleSet>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c6f0-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0c6f0-107">DESCRIPTION</span></span>
<span data-ttu-id="0c6f0-108">Il cmdlet **New-AzCognitiveServicesAccount** crea un account di servizi cognitivi con il tipo e SKU specificati.</span><span class="sxs-lookup"><span data-stu-id="0c6f0-108">The **New-AzCognitiveServicesAccount** cmdlet creates a Cognitive Services account with the specified type and SKU.</span></span>

## <span data-ttu-id="0c6f0-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0c6f0-109">EXAMPLES</span></span>

### <span data-ttu-id="0c6f0-110">1:</span><span class="sxs-lookup"><span data-stu-id="0c6f0-110">1:</span></span>
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

## <span data-ttu-id="0c6f0-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0c6f0-111">PARAMETERS</span></span>

### <span data-ttu-id="0c6f0-112">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="0c6f0-112">-AssignIdentity</span></span>
<span data-ttu-id="0c6f0-113">Genera e assegna una nuova identità di account di servizi cognitivi per questo account di archiviazione per l'uso con i servizi di gestione delle chiavi, come Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="0c6f0-113">Generate and assign a new Cognitive Services Account Identity for this storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="0c6f0-114">-CognitiveServicesEncryption</span><span class="sxs-lookup"><span data-stu-id="0c6f0-114">-CognitiveServicesEncryption</span></span>
<span data-ttu-id="0c6f0-115">Se impostare la fonte di crittografia dell'account dei servizi cognitivi in Microsoft. CognitiveServices o meno.</span><span class="sxs-lookup"><span data-stu-id="0c6f0-115">Whether to set Cognitive Services Account Encryption KeySource to Microsoft.CognitiveServices or not.</span></span>

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

### <span data-ttu-id="0c6f0-116">-CustomSubdomainName</span><span class="sxs-lookup"><span data-stu-id="0c6f0-116">-CustomSubdomainName</span></span>
<span data-ttu-id="0c6f0-117">Nome del sottodominio account dei servizi cognitivi.</span><span class="sxs-lookup"><span data-stu-id="0c6f0-117">Cognitive Services Account Subdomain Name.</span></span>

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

### <span data-ttu-id="0c6f0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c6f0-118">-DefaultProfile</span></span>
<span data-ttu-id="0c6f0-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="0c6f0-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0c6f0-120">-Force</span><span class="sxs-lookup"><span data-stu-id="0c6f0-120">-Force</span></span>
<span data-ttu-id="0c6f0-121">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="0c6f0-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0c6f0-122">-Nome di file</span><span class="sxs-lookup"><span data-stu-id="0c6f0-122">-KeyName</span></span>
<span data-ttu-id="0c6f0-123">Account dei servizi cognitivi cifratura del nome del Vault</span><span class="sxs-lookup"><span data-stu-id="0c6f0-123">Cognitive Services Account encryption keySource KeyVault KeyName</span></span>

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

### <span data-ttu-id="0c6f0-124">-KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="0c6f0-124">-KeyVaultEncryption</span></span>
<span data-ttu-id="0c6f0-125">Se impostare la fonte di crittografia dell'account dei servizi cognitivi in Microsoft. Vault o meno.</span><span class="sxs-lookup"><span data-stu-id="0c6f0-125">Whether to set Cognitive Services Account encryption keySource to Microsoft.KeyVault or not.</span></span> <span data-ttu-id="0c6f0-126">Se specifichi il nome di codice, la versione di base e la KeyVaultUri, la fonte di crittografia dell'account dei servizi cognitivi sarà impostata anche su Microsoft. tempo del Vault questo parametro è impostato o meno.</span><span class="sxs-lookup"><span data-stu-id="0c6f0-126">If you specify KeyName, KeyVersion and KeyVaultUri, Cognitive Services Account Encryption KeySource will also be set to Microsoft.KeyVault weather this parameter is set or not.</span></span>

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

### <span data-ttu-id="0c6f0-127">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="0c6f0-127">-KeyVaultUri</span></span>
<span data-ttu-id="0c6f0-128">Account dei servizi cognitivi crittografia della sorgente di KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="0c6f0-128">Cognitive Services Account encryption keySource KeyVault KeyVaultUri</span></span>

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

### <span data-ttu-id="0c6f0-129">-Versione</span><span class="sxs-lookup"><span data-stu-id="0c6f0-129">-KeyVersion</span></span>
<span data-ttu-id="0c6f0-130">Accounting dei servizi cognitivi crittografia della versione di base del Vault</span><span class="sxs-lookup"><span data-stu-id="0c6f0-130">Cognitive Services Account encryption keySource KeyVault KeyVersion</span></span>

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

### <span data-ttu-id="0c6f0-131">-Posizione</span><span class="sxs-lookup"><span data-stu-id="0c6f0-131">-Location</span></span>
<span data-ttu-id="0c6f0-132">Specifica la posizione in cui creare l'account.</span><span class="sxs-lookup"><span data-stu-id="0c6f0-132">Specifies the location in which to create the account.</span></span>

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

### <span data-ttu-id="0c6f0-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="0c6f0-133">-Name</span></span>
<span data-ttu-id="0c6f0-134">Specifica il nome dell'account.</span><span class="sxs-lookup"><span data-stu-id="0c6f0-134">Specifies the name for the account.</span></span>

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

### <span data-ttu-id="0c6f0-135">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="0c6f0-135">-NetworkRuleSet</span></span>
<span data-ttu-id="0c6f0-136">NetworkRuleSet viene usato per definire un set di regole di configurazione per i firewall e le reti virtuali, nonché per impostare i valori per le proprietà di rete, ad esempio come gestire le richieste che non corrispondono a nessuna delle regole definite</span><span class="sxs-lookup"><span data-stu-id="0c6f0-136">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as how to handle requests that don't match any of the defined rules</span></span>

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

### <span data-ttu-id="0c6f0-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c6f0-137">-ResourceGroupName</span></span>
<span data-ttu-id="0c6f0-138">Specifica il nome del gruppo di risorse a cui assegnare l'account.</span><span class="sxs-lookup"><span data-stu-id="0c6f0-138">Specifies the name of the resource group to which to assign the account.</span></span>
<span data-ttu-id="0c6f0-139">Il gruppo di risorse deve già esistere.</span><span class="sxs-lookup"><span data-stu-id="0c6f0-139">The resource group must already exist.</span></span>

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

### <span data-ttu-id="0c6f0-140">-SkuName</span><span class="sxs-lookup"><span data-stu-id="0c6f0-140">-SkuName</span></span>
<span data-ttu-id="0c6f0-141">Specifica l'USK per l'account.</span><span class="sxs-lookup"><span data-stu-id="0c6f0-141">Specifies the SKU for the account.</span></span>
<span data-ttu-id="0c6f0-142">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="0c6f0-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0c6f0-143">F0 (livello gratuito)</span><span class="sxs-lookup"><span data-stu-id="0c6f0-143">F0 (free tier)</span></span>
- <span data-ttu-id="0c6f0-144">S0</span><span class="sxs-lookup"><span data-stu-id="0c6f0-144">S0</span></span>
- <span data-ttu-id="0c6f0-145">S1</span><span class="sxs-lookup"><span data-stu-id="0c6f0-145">S1</span></span>
- <span data-ttu-id="0c6f0-146">S2</span><span class="sxs-lookup"><span data-stu-id="0c6f0-146">S2</span></span>
- <span data-ttu-id="0c6f0-147">S3</span><span class="sxs-lookup"><span data-stu-id="0c6f0-147">S3</span></span>
- <span data-ttu-id="0c6f0-148">S4 per altre informazioni, vedere [API del servizio cognitivo](https://www.microsoft.com/cognitive-services/en-us/apis).</span><span class="sxs-lookup"><span data-stu-id="0c6f0-148">S4 For more information, see [Cognitive Service APIs](https://www.microsoft.com/cognitive-services/en-us/apis).</span></span>

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

### <span data-ttu-id="0c6f0-149">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="0c6f0-149">-StorageAccountId</span></span>
<span data-ttu-id="0c6f0-150">Elenco di account di archiviazione di proprietà dell'utente.</span><span class="sxs-lookup"><span data-stu-id="0c6f0-150">List of User Owned Storage Accounts.</span></span>

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

### <span data-ttu-id="0c6f0-151">-Tag</span><span class="sxs-lookup"><span data-stu-id="0c6f0-151">-Tag</span></span>
<span data-ttu-id="0c6f0-152">Specifica un contrassegno come coppia nome/valore.</span><span class="sxs-lookup"><span data-stu-id="0c6f0-152">Specifies a tag as a name/value pair.</span></span>

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

### <span data-ttu-id="0c6f0-153">-Digitare</span><span class="sxs-lookup"><span data-stu-id="0c6f0-153">-Type</span></span>
<span data-ttu-id="0c6f0-154">Specifica il tipo di account da creare.</span><span class="sxs-lookup"><span data-stu-id="0c6f0-154">Specifies the type of account to create.</span></span> <span data-ttu-id="0c6f0-155">USA `Get-AzCognitiveServicesAccountType` cmdlet per ottenere i valori accettabili correnti.</span><span class="sxs-lookup"><span data-stu-id="0c6f0-155">Use `Get-AzCognitiveServicesAccountType` cmdlet to get current acceptable values.</span></span>

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

### <span data-ttu-id="0c6f0-156">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0c6f0-156">-Confirm</span></span>
<span data-ttu-id="0c6f0-157">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c6f0-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c6f0-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c6f0-158">-WhatIf</span></span>
<span data-ttu-id="0c6f0-159">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0c6f0-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c6f0-160">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0c6f0-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c6f0-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c6f0-161">CommonParameters</span></span>
<span data-ttu-id="0c6f0-162">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c6f0-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c6f0-163">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0c6f0-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c6f0-164">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0c6f0-164">INPUTS</span></span>

### <span data-ttu-id="0c6f0-165">System. String</span><span class="sxs-lookup"><span data-stu-id="0c6f0-165">System.String</span></span>

## <span data-ttu-id="0c6f0-166">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0c6f0-166">OUTPUTS</span></span>

### <span data-ttu-id="0c6f0-167">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="0c6f0-167">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="0c6f0-168">Note</span><span class="sxs-lookup"><span data-stu-id="0c6f0-168">NOTES</span></span>

## <span data-ttu-id="0c6f0-169">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0c6f0-169">RELATED LINKS</span></span>

[<span data-ttu-id="0c6f0-170">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="0c6f0-170">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="0c6f0-171">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="0c6f0-171">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)

[<span data-ttu-id="0c6f0-172">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="0c6f0-172">Set-AzCognitiveServicesAccount</span></span>](./Set-AzCognitiveServicesAccount.md)
