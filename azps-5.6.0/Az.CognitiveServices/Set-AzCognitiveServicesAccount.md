---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 11E2D82A-1DF1-4E19-8328-44674641D1BB
online version: https://docs.microsoft.com/powershell/module/az.cognitiveservices/set-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Set-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Set-AzCognitiveServicesAccount.md
ms.openlocfilehash: 2c995157b56bafb56df7b385c250b6f7c4fdd4e0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991687"
---
# <span data-ttu-id="22ed4-101">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="22ed4-101">Set-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="22ed4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22ed4-102">SYNOPSIS</span></span>
<span data-ttu-id="22ed4-103">Modifica un account.</span><span class="sxs-lookup"><span data-stu-id="22ed4-103">Modifies an account.</span></span>

## <span data-ttu-id="22ed4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="22ed4-104">SYNTAX</span></span>

### <span data-ttu-id="22ed4-105">CognitiveServicesEncryption (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="22ed4-105">CognitiveServicesEncryption (Default)</span></span>
```
Set-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-CustomSubdomainName <String>] [-AssignIdentity] [-IdentityType <IdentityType>]
 [-StorageAccountId <String[]>] [-CognitiveServicesEncryption] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-PublicNetworkAccess <String>] [-ApiProperty <CognitiveServicesAccountApiProperties>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22ed4-106">KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="22ed4-106">KeyVaultEncryption</span></span>
```
Set-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-CustomSubdomainName <String>] [-AssignIdentity] [-IdentityType <IdentityType>]
 [-StorageAccountId <String[]>] [-KeyVaultEncryption] -KeyName <String> -KeyVersion <String>
 -KeyVaultUri <String> [-NetworkRuleSet <PSNetworkRuleSet>] [-PublicNetworkAccess <String>]
 [-ApiProperty <CognitiveServicesAccountApiProperties>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22ed4-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="22ed4-107">DESCRIPTION</span></span>
<span data-ttu-id="22ed4-108">Il cmdlet **Set-AzCognitiveServicesAccount** modifica lo SKU o i tag dell'account di Servizi cognitivi specificato.</span><span class="sxs-lookup"><span data-stu-id="22ed4-108">The **Set-AzCognitiveServicesAccount** cmdlet modifies the SKU or tags of the specified Cognitive Services account.</span></span>

## <span data-ttu-id="22ed4-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="22ed4-109">EXAMPLES</span></span>

### <span data-ttu-id="22ed4-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="22ed4-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis -SkuName S0


ResourceGroupName : cognitive-services-resource-group
AccountName       : myluis
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/cognitive-services-resource-group/providers/Microsoft.Cog
                    nitiveServices/accounts/myluis
Endpoint          : https://westus.api.cognitive.microsoft.com/luis/v2.0
Location          : WESTUS
Sku               : Microsoft.Azure.Management.CognitiveServices.Models.Sku
AccountType       : LUIS
ResourceType      : Microsoft.CognitiveServices/accounts
Etag              : "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
ProvisioningState : Succeeded
Tags              :
```

## <span data-ttu-id="22ed4-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="22ed4-111">PARAMETERS</span></span>

### <span data-ttu-id="22ed4-112">-ApiProperty</span><span class="sxs-lookup"><span data-stu-id="22ed4-112">-ApiProperty</span></span>
<span data-ttu-id="22ed4-113">ApiProperties dell'account di Servizi cognitivi.</span><span class="sxs-lookup"><span data-stu-id="22ed4-113">The ApiProperties of Cognitive Services Account.</span></span> <span data-ttu-id="22ed4-114">Obbligatorio per tipi di account specifici.</span><span class="sxs-lookup"><span data-stu-id="22ed4-114">Required by specific account types.</span></span>

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

### <span data-ttu-id="22ed4-115">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="22ed4-115">-AssignIdentity</span></span>
<span data-ttu-id="22ed4-116">Generare e assegnare una nuova identità dell'account di Servizi cognitivi per questo account di archiviazione per l'uso con servizi di gestione delle chiavi come Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="22ed4-116">Generate and assign a new Cognitive Services Account Identity for this storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="22ed4-117">-CognitiveServicesEncryption</span><span class="sxs-lookup"><span data-stu-id="22ed4-117">-CognitiveServicesEncryption</span></span>
<span data-ttu-id="22ed4-118">Se impostare o meno KeySource di crittografia dell'account dei Servizi cognitivi su Microsoft.CognitiveServices.</span><span class="sxs-lookup"><span data-stu-id="22ed4-118">Whether to set Cognitive Services Account Encryption KeySource to Microsoft.CognitiveServices or not.</span></span>

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

### <span data-ttu-id="22ed4-119">-CustomSubdomainName</span><span class="sxs-lookup"><span data-stu-id="22ed4-119">-CustomSubdomainName</span></span>
<span data-ttu-id="22ed4-120">Nome sottodominio account di Servizi cognitivi.</span><span class="sxs-lookup"><span data-stu-id="22ed4-120">Cognitive Services Account Subdomain Name.</span></span>

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

### <span data-ttu-id="22ed4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22ed4-121">-DefaultProfile</span></span>
<span data-ttu-id="22ed4-122">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="22ed4-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="22ed4-123">-Force</span><span class="sxs-lookup"><span data-stu-id="22ed4-123">-Force</span></span>
<span data-ttu-id="22ed4-124">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="22ed4-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="22ed4-125">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="22ed4-125">-IdentityType</span></span>
<span data-ttu-id="22ed4-126">Tipo di identità del servizio gestito.</span><span class="sxs-lookup"><span data-stu-id="22ed4-126">Type of managed service identity.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.CognitiveServices.Models.IdentityType]
Parameter Sets: (All)
Aliases:
Accepted values: None, SystemAssigned, UserAssigned

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22ed4-127">-KeyName</span><span class="sxs-lookup"><span data-stu-id="22ed4-127">-KeyName</span></span>
<span data-ttu-id="22ed4-128">Chiave di crittografia dell'account di Servizi cognitiviSource KeyVault KeyName</span><span class="sxs-lookup"><span data-stu-id="22ed4-128">Cognitive Services Account encryption keySource KeyVault KeyName</span></span>

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

### <span data-ttu-id="22ed4-129">-KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="22ed4-129">-KeyVaultEncryption</span></span>
<span data-ttu-id="22ed4-130">Se impostare o meno la chiave di crittografia dell'account dei servizi cognitivi su Microsoft.KeyVault.</span><span class="sxs-lookup"><span data-stu-id="22ed4-130">Whether to set Cognitive Services Account encryption keySource to Microsoft.KeyVault or not.</span></span> <span data-ttu-id="22ed4-131">Se si specifica KeyName, KeyVersion e KeyVaultUri, anche Cognitive Services Account Encryption KeySource verrà impostato su Microsoft.KeyVault meteo che questo parametro è impostato o meno.</span><span class="sxs-lookup"><span data-stu-id="22ed4-131">If you specify KeyName, KeyVersion and KeyVaultUri, Cognitive Services Account Encryption KeySource will also be set to Microsoft.KeyVault weather this parameter is set or not.</span></span>

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

### <span data-ttu-id="22ed4-132">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="22ed4-132">-KeyVaultUri</span></span>
<span data-ttu-id="22ed4-133">Chiave di crittografia dell'account dei servizi cognitiviSource KeyVault KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="22ed4-133">Cognitive Services Account encryption keySource KeyVault KeyVaultUri</span></span>

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

### <span data-ttu-id="22ed4-134">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="22ed4-134">-KeyVersion</span></span>
<span data-ttu-id="22ed4-135">Chiave di crittografia dell'account dei servizi cognitiviSource KeyVault KeyVersion</span><span class="sxs-lookup"><span data-stu-id="22ed4-135">Cognitive Services Account encryption keySource KeyVault KeyVersion</span></span>

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

### <span data-ttu-id="22ed4-136">-Name</span><span class="sxs-lookup"><span data-stu-id="22ed4-136">-Name</span></span>
<span data-ttu-id="22ed4-137">Specifica il nome dell'account da modificare.</span><span class="sxs-lookup"><span data-stu-id="22ed4-137">Specifies the name of the account to modify.</span></span>

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

### <span data-ttu-id="22ed4-138">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="22ed4-138">-NetworkRuleSet</span></span>
<span data-ttu-id="22ed4-139">NetworkRuleSet viene usato per definire un set di regole di configurazione per firewall e reti virtuali, oltre che per impostare valori per le proprietà di rete, ad esempio come gestire le richieste che non corrispondono a nessuna delle regole definite</span><span class="sxs-lookup"><span data-stu-id="22ed4-139">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as how to handle requests that don't match any of the defined rules</span></span>

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

### <span data-ttu-id="22ed4-140">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="22ed4-140">-PublicNetworkAccess</span></span>
<span data-ttu-id="22ed4-141">Tipo di accesso di rete per l'account di Servizi cognitivi.</span><span class="sxs-lookup"><span data-stu-id="22ed4-141">The network access type for Cognitive Services Account.</span></span>

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

### <span data-ttu-id="22ed4-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22ed4-142">-ResourceGroupName</span></span>
<span data-ttu-id="22ed4-143">Specifica il nome del gruppo di risorse a cui è assegnato l'account.</span><span class="sxs-lookup"><span data-stu-id="22ed4-143">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="22ed4-144">-SKUName</span><span class="sxs-lookup"><span data-stu-id="22ed4-144">-SkuName</span></span>
<span data-ttu-id="22ed4-145">Specifica lo SKU per l'account.</span><span class="sxs-lookup"><span data-stu-id="22ed4-145">Specifies the SKU for the account.</span></span>
<span data-ttu-id="22ed4-146">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="22ed4-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="22ed4-147">F0 (livello gratuito)</span><span class="sxs-lookup"><span data-stu-id="22ed4-147">F0 (free tier)</span></span>
- <span data-ttu-id="22ed4-148">S0</span><span class="sxs-lookup"><span data-stu-id="22ed4-148">S0</span></span>
- <span data-ttu-id="22ed4-149">S1</span><span class="sxs-lookup"><span data-stu-id="22ed4-149">S1</span></span>
- <span data-ttu-id="22ed4-150">S2</span><span class="sxs-lookup"><span data-stu-id="22ed4-150">S2</span></span>
- <span data-ttu-id="22ed4-151">S3</span><span class="sxs-lookup"><span data-stu-id="22ed4-151">S3</span></span>
- <span data-ttu-id="22ed4-152">S4</span><span class="sxs-lookup"><span data-stu-id="22ed4-152">S4</span></span>

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

### <span data-ttu-id="22ed4-153">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="22ed4-153">-StorageAccountId</span></span>
<span data-ttu-id="22ed4-154">Elenco degli account di archiviazione di proprietà dell'utente.</span><span class="sxs-lookup"><span data-stu-id="22ed4-154">List of User Owned Storage Accounts.</span></span>

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

### <span data-ttu-id="22ed4-155">-Tag</span><span class="sxs-lookup"><span data-stu-id="22ed4-155">-Tag</span></span>
<span data-ttu-id="22ed4-156">Specifica un tag come coppia nome/valore.</span><span class="sxs-lookup"><span data-stu-id="22ed4-156">Specifies a tag as a name/value pair.</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22ed4-157">-Confirm</span><span class="sxs-lookup"><span data-stu-id="22ed4-157">-Confirm</span></span>
<span data-ttu-id="22ed4-158">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="22ed4-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22ed4-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22ed4-159">-WhatIf</span></span>
<span data-ttu-id="22ed4-160">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="22ed4-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22ed4-161">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="22ed4-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22ed4-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22ed4-162">CommonParameters</span></span>
<span data-ttu-id="22ed4-163">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22ed4-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22ed4-164">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="22ed4-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22ed4-165">INPUT</span><span class="sxs-lookup"><span data-stu-id="22ed4-165">INPUTS</span></span>

### <span data-ttu-id="22ed4-166">System.String</span><span class="sxs-lookup"><span data-stu-id="22ed4-166">System.String</span></span>

### <span data-ttu-id="22ed4-167">System.Collections.Hashtable[]</span><span class="sxs-lookup"><span data-stu-id="22ed4-167">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="22ed4-168">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="22ed4-168">OUTPUTS</span></span>

### <span data-ttu-id="22ed4-169">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="22ed4-169">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="22ed4-170">NOTE</span><span class="sxs-lookup"><span data-stu-id="22ed4-170">NOTES</span></span>

## <span data-ttu-id="22ed4-171">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="22ed4-171">RELATED LINKS</span></span>

[<span data-ttu-id="22ed4-172">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="22ed4-172">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="22ed4-173">New-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="22ed4-173">New-AzCognitiveServicesAccount</span></span>](./New-AzCognitiveServicesAccount.md)

[<span data-ttu-id="22ed4-174">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="22ed4-174">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)
