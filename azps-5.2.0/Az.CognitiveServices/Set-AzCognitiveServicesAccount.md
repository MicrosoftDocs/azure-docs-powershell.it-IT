---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 11E2D82A-1DF1-4E19-8328-44674641D1BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/set-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Set-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Set-AzCognitiveServicesAccount.md
ms.openlocfilehash: 5cfbfa0452fba4d01d2af5aa8e6acc3a141a4426
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358315"
---
# <span data-ttu-id="95918-101">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="95918-101">Set-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="95918-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="95918-102">SYNOPSIS</span></span>
<span data-ttu-id="95918-103">Modifica un account.</span><span class="sxs-lookup"><span data-stu-id="95918-103">Modifies an account.</span></span>

## <span data-ttu-id="95918-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="95918-104">SYNTAX</span></span>

### <span data-ttu-id="95918-105">CognitiveServicesEncryption (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="95918-105">CognitiveServicesEncryption (Default)</span></span>
```
Set-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-CustomSubdomainName <String>] [-AssignIdentity] [-IdentityType <IdentityType>]
 [-StorageAccountId <String[]>] [-CognitiveServicesEncryption] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-PublicNetworkAccess <String>] [-ApiProperty <CognitiveServicesAccountApiProperties>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95918-106">KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="95918-106">KeyVaultEncryption</span></span>
```
Set-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-CustomSubdomainName <String>] [-AssignIdentity] [-IdentityType <IdentityType>]
 [-StorageAccountId <String[]>] [-KeyVaultEncryption] -KeyName <String> -KeyVersion <String>
 -KeyVaultUri <String> [-NetworkRuleSet <PSNetworkRuleSet>] [-PublicNetworkAccess <String>]
 [-ApiProperty <CognitiveServicesAccountApiProperties>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95918-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="95918-107">DESCRIPTION</span></span>
<span data-ttu-id="95918-108">Il cmdlet **set-AzCognitiveServicesAccount** modifica l'USK o i tag dell'account dei servizi cognitivi specificati.</span><span class="sxs-lookup"><span data-stu-id="95918-108">The **Set-AzCognitiveServicesAccount** cmdlet modifies the SKU or tags of the specified Cognitive Services account.</span></span>

## <span data-ttu-id="95918-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="95918-109">EXAMPLES</span></span>

### <span data-ttu-id="95918-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="95918-110">Example 1</span></span>
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

## <span data-ttu-id="95918-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="95918-111">PARAMETERS</span></span>

### <span data-ttu-id="95918-112">-ApiProperty</span><span class="sxs-lookup"><span data-stu-id="95918-112">-ApiProperty</span></span>
<span data-ttu-id="95918-113">L'account di ApiProperties of cognitive Services.</span><span class="sxs-lookup"><span data-stu-id="95918-113">The ApiProperties of Cognitive Services Account.</span></span> <span data-ttu-id="95918-114">Obbligatorio per tipi di account specifici.</span><span class="sxs-lookup"><span data-stu-id="95918-114">Required by specific account types.</span></span>

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

### <span data-ttu-id="95918-115">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="95918-115">-AssignIdentity</span></span>
<span data-ttu-id="95918-116">Genera e assegna una nuova identità di account di servizi cognitivi per questo account di archiviazione per l'uso con i servizi di gestione delle chiavi, come Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="95918-116">Generate and assign a new Cognitive Services Account Identity for this storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="95918-117">-CognitiveServicesEncryption</span><span class="sxs-lookup"><span data-stu-id="95918-117">-CognitiveServicesEncryption</span></span>
<span data-ttu-id="95918-118">Se impostare la fonte di crittografia dell'account dei servizi cognitivi in Microsoft. CognitiveServices o meno.</span><span class="sxs-lookup"><span data-stu-id="95918-118">Whether to set Cognitive Services Account Encryption KeySource to Microsoft.CognitiveServices or not.</span></span>

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

### <span data-ttu-id="95918-119">-CustomSubdomainName</span><span class="sxs-lookup"><span data-stu-id="95918-119">-CustomSubdomainName</span></span>
<span data-ttu-id="95918-120">Nome del sottodominio account dei servizi cognitivi.</span><span class="sxs-lookup"><span data-stu-id="95918-120">Cognitive Services Account Subdomain Name.</span></span>

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

### <span data-ttu-id="95918-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95918-121">-DefaultProfile</span></span>
<span data-ttu-id="95918-122">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="95918-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="95918-123">-Force</span><span class="sxs-lookup"><span data-stu-id="95918-123">-Force</span></span>
<span data-ttu-id="95918-124">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="95918-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="95918-125">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="95918-125">-IdentityType</span></span>
<span data-ttu-id="95918-126">Tipo di identità del servizio gestito.</span><span class="sxs-lookup"><span data-stu-id="95918-126">Type of managed service identity.</span></span>

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

### <span data-ttu-id="95918-127">-Nome di file</span><span class="sxs-lookup"><span data-stu-id="95918-127">-KeyName</span></span>
<span data-ttu-id="95918-128">Account dei servizi cognitivi cifratura del nome del Vault</span><span class="sxs-lookup"><span data-stu-id="95918-128">Cognitive Services Account encryption keySource KeyVault KeyName</span></span>

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

### <span data-ttu-id="95918-129">-KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="95918-129">-KeyVaultEncryption</span></span>
<span data-ttu-id="95918-130">Se impostare la fonte di crittografia dell'account dei servizi cognitivi in Microsoft. Vault o meno.</span><span class="sxs-lookup"><span data-stu-id="95918-130">Whether to set Cognitive Services Account encryption keySource to Microsoft.KeyVault or not.</span></span> <span data-ttu-id="95918-131">Se specifichi il nome di codice, la versione di base e la KeyVaultUri, la fonte di crittografia dell'account dei servizi cognitivi sarà impostata anche su Microsoft. tempo del Vault questo parametro è impostato o meno.</span><span class="sxs-lookup"><span data-stu-id="95918-131">If you specify KeyName, KeyVersion and KeyVaultUri, Cognitive Services Account Encryption KeySource will also be set to Microsoft.KeyVault weather this parameter is set or not.</span></span>

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

### <span data-ttu-id="95918-132">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="95918-132">-KeyVaultUri</span></span>
<span data-ttu-id="95918-133">Account dei servizi cognitivi crittografia della sorgente di KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="95918-133">Cognitive Services Account encryption keySource KeyVault KeyVaultUri</span></span>

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

### <span data-ttu-id="95918-134">-Versione</span><span class="sxs-lookup"><span data-stu-id="95918-134">-KeyVersion</span></span>
<span data-ttu-id="95918-135">Accounting dei servizi cognitivi crittografia della versione di base del Vault</span><span class="sxs-lookup"><span data-stu-id="95918-135">Cognitive Services Account encryption keySource KeyVault KeyVersion</span></span>

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

### <span data-ttu-id="95918-136">-Nome</span><span class="sxs-lookup"><span data-stu-id="95918-136">-Name</span></span>
<span data-ttu-id="95918-137">Specifica il nome dell'account da modificare.</span><span class="sxs-lookup"><span data-stu-id="95918-137">Specifies the name of the account to modify.</span></span>

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

### <span data-ttu-id="95918-138">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="95918-138">-NetworkRuleSet</span></span>
<span data-ttu-id="95918-139">NetworkRuleSet viene usato per definire un set di regole di configurazione per i firewall e le reti virtuali, nonché per impostare i valori per le proprietà di rete, ad esempio come gestire le richieste che non corrispondono a nessuna delle regole definite</span><span class="sxs-lookup"><span data-stu-id="95918-139">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as how to handle requests that don't match any of the defined rules</span></span>

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

### <span data-ttu-id="95918-140">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="95918-140">-PublicNetworkAccess</span></span>
<span data-ttu-id="95918-141">Il tipo di accesso alla rete per l'account dei servizi cognitivi.</span><span class="sxs-lookup"><span data-stu-id="95918-141">The network access type for Cognitive Services Account.</span></span>

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

### <span data-ttu-id="95918-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95918-142">-ResourceGroupName</span></span>
<span data-ttu-id="95918-143">Specifica il nome del gruppo di risorse a cui è assegnato l'account.</span><span class="sxs-lookup"><span data-stu-id="95918-143">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="95918-144">-SkuName</span><span class="sxs-lookup"><span data-stu-id="95918-144">-SkuName</span></span>
<span data-ttu-id="95918-145">Specifica l'USK per l'account.</span><span class="sxs-lookup"><span data-stu-id="95918-145">Specifies the SKU for the account.</span></span>
<span data-ttu-id="95918-146">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="95918-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="95918-147">F0 (livello gratuito)</span><span class="sxs-lookup"><span data-stu-id="95918-147">F0 (free tier)</span></span>
- <span data-ttu-id="95918-148">S0</span><span class="sxs-lookup"><span data-stu-id="95918-148">S0</span></span>
- <span data-ttu-id="95918-149">S1</span><span class="sxs-lookup"><span data-stu-id="95918-149">S1</span></span>
- <span data-ttu-id="95918-150">S2</span><span class="sxs-lookup"><span data-stu-id="95918-150">S2</span></span>
- <span data-ttu-id="95918-151">S3</span><span class="sxs-lookup"><span data-stu-id="95918-151">S3</span></span>
- <span data-ttu-id="95918-152">S4</span><span class="sxs-lookup"><span data-stu-id="95918-152">S4</span></span>

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

### <span data-ttu-id="95918-153">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="95918-153">-StorageAccountId</span></span>
<span data-ttu-id="95918-154">Elenco di account di archiviazione di proprietà dell'utente.</span><span class="sxs-lookup"><span data-stu-id="95918-154">List of User Owned Storage Accounts.</span></span>

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

### <span data-ttu-id="95918-155">-Tag</span><span class="sxs-lookup"><span data-stu-id="95918-155">-Tag</span></span>
<span data-ttu-id="95918-156">Specifica un contrassegno come coppia nome/valore.</span><span class="sxs-lookup"><span data-stu-id="95918-156">Specifies a tag as a name/value pair.</span></span>

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

### <span data-ttu-id="95918-157">-Confermare</span><span class="sxs-lookup"><span data-stu-id="95918-157">-Confirm</span></span>
<span data-ttu-id="95918-158">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="95918-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95918-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95918-159">-WhatIf</span></span>
<span data-ttu-id="95918-160">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="95918-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95918-161">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="95918-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95918-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95918-162">CommonParameters</span></span>
<span data-ttu-id="95918-163">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95918-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95918-164">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="95918-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95918-165">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="95918-165">INPUTS</span></span>

### <span data-ttu-id="95918-166">System. String</span><span class="sxs-lookup"><span data-stu-id="95918-166">System.String</span></span>

### <span data-ttu-id="95918-167">System. Collections. Hashtable []</span><span class="sxs-lookup"><span data-stu-id="95918-167">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="95918-168">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="95918-168">OUTPUTS</span></span>

### <span data-ttu-id="95918-169">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="95918-169">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="95918-170">Note</span><span class="sxs-lookup"><span data-stu-id="95918-170">NOTES</span></span>

## <span data-ttu-id="95918-171">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="95918-171">RELATED LINKS</span></span>

[<span data-ttu-id="95918-172">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="95918-172">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="95918-173">New-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="95918-173">New-AzCognitiveServicesAccount</span></span>](./New-AzCognitiveServicesAccount.md)

[<span data-ttu-id="95918-174">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="95918-174">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)
