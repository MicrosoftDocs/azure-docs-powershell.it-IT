---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: A2B4ACC1-6F53-47DE-A2D4-831E8AC89A5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/new-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccount.md
ms.openlocfilehash: d19c22ffd0be5b6ea935b832d847bb74661e3106
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675500"
---
# <span data-ttu-id="6cb10-101">New-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="6cb10-101">New-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="6cb10-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6cb10-102">SYNOPSIS</span></span>
<span data-ttu-id="6cb10-103">Crea un account di servizi cognitivi.</span><span class="sxs-lookup"><span data-stu-id="6cb10-103">Creates a Cognitive Services account.</span></span>

## <span data-ttu-id="6cb10-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6cb10-104">SYNTAX</span></span>

```
New-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-CustomSubdomainName <String>]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6cb10-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6cb10-105">DESCRIPTION</span></span>
<span data-ttu-id="6cb10-106">Il cmdlet **New-AzCognitiveServicesAccount** crea un account di servizi cognitivi con il tipo e SKU specificati.</span><span class="sxs-lookup"><span data-stu-id="6cb10-106">The **New-AzCognitiveServicesAccount** cmdlet creates a Cognitive Services account with the specified type and SKU.</span></span>

## <span data-ttu-id="6cb10-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6cb10-107">EXAMPLES</span></span>

### <span data-ttu-id="6cb10-108">1:</span><span class="sxs-lookup"><span data-stu-id="6cb10-108">1:</span></span>
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

## <span data-ttu-id="6cb10-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6cb10-109">PARAMETERS</span></span>

### <span data-ttu-id="6cb10-110">-CustomSubdomainName</span><span class="sxs-lookup"><span data-stu-id="6cb10-110">-CustomSubdomainName</span></span>
<span data-ttu-id="6cb10-111">Nome del sottodominio account dei servizi cognitivi.</span><span class="sxs-lookup"><span data-stu-id="6cb10-111">Cognitive Services Account Subdomain Name.</span></span>

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

### <span data-ttu-id="6cb10-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cb10-112">-DefaultProfile</span></span>
<span data-ttu-id="6cb10-113">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="6cb10-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6cb10-114">-Force</span><span class="sxs-lookup"><span data-stu-id="6cb10-114">-Force</span></span>
<span data-ttu-id="6cb10-115">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="6cb10-115">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6cb10-116">-Posizione</span><span class="sxs-lookup"><span data-stu-id="6cb10-116">-Location</span></span>
<span data-ttu-id="6cb10-117">Specifica la posizione in cui creare l'account.</span><span class="sxs-lookup"><span data-stu-id="6cb10-117">Specifies the location in which to create the account.</span></span>

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

### <span data-ttu-id="6cb10-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="6cb10-118">-Name</span></span>
<span data-ttu-id="6cb10-119">Specifica il nome dell'account.</span><span class="sxs-lookup"><span data-stu-id="6cb10-119">Specifies the name for the account.</span></span>

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

### <span data-ttu-id="6cb10-120">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="6cb10-120">-NetworkRuleSet</span></span>
<span data-ttu-id="6cb10-121">NetworkRuleSet viene usato per definire un set di regole di configurazione per i firewall e le reti virtuali, nonché per impostare i valori per le proprietà di rete, ad esempio come gestire le richieste che non corrispondono a nessuna delle regole definite</span><span class="sxs-lookup"><span data-stu-id="6cb10-121">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as how to handle requests that don't match any of the defined rules</span></span>

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

### <span data-ttu-id="6cb10-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cb10-122">-ResourceGroupName</span></span>
<span data-ttu-id="6cb10-123">Specifica il nome del gruppo di risorse a cui assegnare l'account.</span><span class="sxs-lookup"><span data-stu-id="6cb10-123">Specifies the name of the resource group to which to assign the account.</span></span>
<span data-ttu-id="6cb10-124">Il gruppo di risorse deve già esistere.</span><span class="sxs-lookup"><span data-stu-id="6cb10-124">The resource group must already exist.</span></span>

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

### <span data-ttu-id="6cb10-125">-SkuName</span><span class="sxs-lookup"><span data-stu-id="6cb10-125">-SkuName</span></span>
<span data-ttu-id="6cb10-126">Specifica l'USK per l'account.</span><span class="sxs-lookup"><span data-stu-id="6cb10-126">Specifies the SKU for the account.</span></span>
<span data-ttu-id="6cb10-127">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="6cb10-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6cb10-128">F0 (livello gratuito)</span><span class="sxs-lookup"><span data-stu-id="6cb10-128">F0 (free tier)</span></span>
- <span data-ttu-id="6cb10-129">S0</span><span class="sxs-lookup"><span data-stu-id="6cb10-129">S0</span></span>
- <span data-ttu-id="6cb10-130">S1</span><span class="sxs-lookup"><span data-stu-id="6cb10-130">S1</span></span>
- <span data-ttu-id="6cb10-131">S2</span><span class="sxs-lookup"><span data-stu-id="6cb10-131">S2</span></span>
- <span data-ttu-id="6cb10-132">S3</span><span class="sxs-lookup"><span data-stu-id="6cb10-132">S3</span></span>
- <span data-ttu-id="6cb10-133">S4 per altre informazioni, vedere [API del servizio cognitivo](https://www.microsoft.com/cognitive-services/en-us/apis).</span><span class="sxs-lookup"><span data-stu-id="6cb10-133">S4 For more information, see [Cognitive Service APIs](https://www.microsoft.com/cognitive-services/en-us/apis).</span></span>

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

### <span data-ttu-id="6cb10-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="6cb10-134">-Tag</span></span>
<span data-ttu-id="6cb10-135">Specifica un contrassegno come coppia nome/valore.</span><span class="sxs-lookup"><span data-stu-id="6cb10-135">Specifies a tag as a name/value pair.</span></span>

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

### <span data-ttu-id="6cb10-136">-Digitare</span><span class="sxs-lookup"><span data-stu-id="6cb10-136">-Type</span></span>
<span data-ttu-id="6cb10-137">Specifica il tipo di account da creare.</span><span class="sxs-lookup"><span data-stu-id="6cb10-137">Specifies the type of account to create.</span></span> <span data-ttu-id="6cb10-138">USA `Get-AzCognitiveServicesAccountType` cmdlet per ottenere i valori accettabili correnti.</span><span class="sxs-lookup"><span data-stu-id="6cb10-138">Use `Get-AzCognitiveServicesAccountType` cmdlet to get current acceptable values.</span></span>

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

### <span data-ttu-id="6cb10-139">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6cb10-139">-Confirm</span></span>
<span data-ttu-id="6cb10-140">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6cb10-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6cb10-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6cb10-141">-WhatIf</span></span>
<span data-ttu-id="6cb10-142">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6cb10-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6cb10-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6cb10-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6cb10-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cb10-144">CommonParameters</span></span>
<span data-ttu-id="6cb10-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cb10-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cb10-146">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6cb10-146">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cb10-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6cb10-147">INPUTS</span></span>

### <span data-ttu-id="6cb10-148">System. String</span><span class="sxs-lookup"><span data-stu-id="6cb10-148">System.String</span></span>

## <span data-ttu-id="6cb10-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6cb10-149">OUTPUTS</span></span>

### <span data-ttu-id="6cb10-150">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="6cb10-150">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="6cb10-151">Note</span><span class="sxs-lookup"><span data-stu-id="6cb10-151">NOTES</span></span>

## <span data-ttu-id="6cb10-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6cb10-152">RELATED LINKS</span></span>

[<span data-ttu-id="6cb10-153">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="6cb10-153">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="6cb10-154">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="6cb10-154">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)

[<span data-ttu-id="6cb10-155">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="6cb10-155">Set-AzCognitiveServicesAccount</span></span>](./Set-AzCognitiveServicesAccount.md)
