---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 11E2D82A-1DF1-4E19-8328-44674641D1BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/set-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Set-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Set-AzCognitiveServicesAccount.md
ms.openlocfilehash: 57d136691d6ca0ac9bcd85f205d70cf267437b7b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675491"
---
# <span data-ttu-id="720aa-101">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="720aa-101">Set-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="720aa-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="720aa-102">SYNOPSIS</span></span>
<span data-ttu-id="720aa-103">Modifica un account.</span><span class="sxs-lookup"><span data-stu-id="720aa-103">Modifies an account.</span></span>

## <span data-ttu-id="720aa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="720aa-104">SYNTAX</span></span>

```
Set-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-CustomSubdomainName <String>] [-NetworkRuleSet <PSNetworkRuleSet>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="720aa-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="720aa-105">DESCRIPTION</span></span>
<span data-ttu-id="720aa-106">Il cmdlet **set-AzCognitiveServicesAccount** modifica l'USK o i tag dell'account dei servizi cognitivi specificati.</span><span class="sxs-lookup"><span data-stu-id="720aa-106">The **Set-AzCognitiveServicesAccount** cmdlet modifies the SKU or tags of the specified Cognitive Services account.</span></span>

## <span data-ttu-id="720aa-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="720aa-107">EXAMPLES</span></span>

### <span data-ttu-id="720aa-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="720aa-108">Example 1</span></span>
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

## <span data-ttu-id="720aa-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="720aa-109">PARAMETERS</span></span>

### <span data-ttu-id="720aa-110">-CustomSubdomainName</span><span class="sxs-lookup"><span data-stu-id="720aa-110">-CustomSubdomainName</span></span>
<span data-ttu-id="720aa-111">Nome del sottodominio account dei servizi cognitivi.</span><span class="sxs-lookup"><span data-stu-id="720aa-111">Cognitive Services Account Subdomain Name.</span></span>

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

### <span data-ttu-id="720aa-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="720aa-112">-DefaultProfile</span></span>
<span data-ttu-id="720aa-113">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="720aa-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="720aa-114">-Force</span><span class="sxs-lookup"><span data-stu-id="720aa-114">-Force</span></span>
<span data-ttu-id="720aa-115">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="720aa-115">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="720aa-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="720aa-116">-Name</span></span>
<span data-ttu-id="720aa-117">Specifica il nome dell'account da modificare.</span><span class="sxs-lookup"><span data-stu-id="720aa-117">Specifies the name of the account to modify.</span></span>

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

### <span data-ttu-id="720aa-118">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="720aa-118">-NetworkRuleSet</span></span>
<span data-ttu-id="720aa-119">NetworkRuleSet viene usato per definire un set di regole di configurazione per i firewall e le reti virtuali, nonché per impostare i valori per le proprietà di rete, ad esempio come gestire le richieste che non corrispondono a nessuna delle regole definite</span><span class="sxs-lookup"><span data-stu-id="720aa-119">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as how to handle requests that don't match any of the defined rules</span></span>

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

### <span data-ttu-id="720aa-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="720aa-120">-ResourceGroupName</span></span>
<span data-ttu-id="720aa-121">Specifica il nome del gruppo di risorse a cui è assegnato l'account.</span><span class="sxs-lookup"><span data-stu-id="720aa-121">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="720aa-122">-SkuName</span><span class="sxs-lookup"><span data-stu-id="720aa-122">-SkuName</span></span>
<span data-ttu-id="720aa-123">Specifica l'USK per l'account.</span><span class="sxs-lookup"><span data-stu-id="720aa-123">Specifies the SKU for the account.</span></span>
<span data-ttu-id="720aa-124">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="720aa-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="720aa-125">F0 (livello gratuito)</span><span class="sxs-lookup"><span data-stu-id="720aa-125">F0 (free tier)</span></span>
- <span data-ttu-id="720aa-126">S0</span><span class="sxs-lookup"><span data-stu-id="720aa-126">S0</span></span>
- <span data-ttu-id="720aa-127">S1</span><span class="sxs-lookup"><span data-stu-id="720aa-127">S1</span></span>
- <span data-ttu-id="720aa-128">S2</span><span class="sxs-lookup"><span data-stu-id="720aa-128">S2</span></span>
- <span data-ttu-id="720aa-129">S3</span><span class="sxs-lookup"><span data-stu-id="720aa-129">S3</span></span>
- <span data-ttu-id="720aa-130">S4</span><span class="sxs-lookup"><span data-stu-id="720aa-130">S4</span></span>

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

### <span data-ttu-id="720aa-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="720aa-131">-Tag</span></span>
<span data-ttu-id="720aa-132">Specifica un contrassegno come coppia nome/valore.</span><span class="sxs-lookup"><span data-stu-id="720aa-132">Specifies a tag as a name/value pair.</span></span>

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

### <span data-ttu-id="720aa-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="720aa-133">-Confirm</span></span>
<span data-ttu-id="720aa-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="720aa-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="720aa-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="720aa-135">-WhatIf</span></span>
<span data-ttu-id="720aa-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="720aa-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="720aa-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="720aa-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="720aa-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="720aa-138">CommonParameters</span></span>
<span data-ttu-id="720aa-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="720aa-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="720aa-140">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="720aa-140">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="720aa-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="720aa-141">INPUTS</span></span>

### <span data-ttu-id="720aa-142">System. String</span><span class="sxs-lookup"><span data-stu-id="720aa-142">System.String</span></span>

### <span data-ttu-id="720aa-143">System. Collections. Hashtable []</span><span class="sxs-lookup"><span data-stu-id="720aa-143">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="720aa-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="720aa-144">OUTPUTS</span></span>

### <span data-ttu-id="720aa-145">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="720aa-145">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="720aa-146">Note</span><span class="sxs-lookup"><span data-stu-id="720aa-146">NOTES</span></span>

## <span data-ttu-id="720aa-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="720aa-147">RELATED LINKS</span></span>

[<span data-ttu-id="720aa-148">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="720aa-148">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="720aa-149">New-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="720aa-149">New-AzCognitiveServicesAccount</span></span>](./New-AzCognitiveServicesAccount.md)

[<span data-ttu-id="720aa-150">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="720aa-150">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)
