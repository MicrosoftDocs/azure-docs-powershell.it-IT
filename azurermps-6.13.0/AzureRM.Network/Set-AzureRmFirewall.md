---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 40E56EC1-3327-4DFF-8262-E2EEBB5E4447
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmFirewall.md
ms.openlocfilehash: 8f2c2560ac8ca0787a8a0eb8d37fb5242f4a915e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507416"
---
# <span data-ttu-id="b00fd-101">Set-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="b00fd-101">Set-AzureRmFirewall</span></span>

## <span data-ttu-id="b00fd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b00fd-102">SYNOPSIS</span></span>
<span data-ttu-id="b00fd-103">Salva un firewall modificato.</span><span class="sxs-lookup"><span data-stu-id="b00fd-103">Saves a modified Firewall.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b00fd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b00fd-104">SYNTAX</span></span>

```
Set-AzureRmFirewall -AzureFirewall <PSAzureFirewall> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b00fd-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b00fd-105">DESCRIPTION</span></span>
<span data-ttu-id="b00fd-106">Il cmdlet **set-AzureRmFirewall** aggiorna un firewall di Azure.</span><span class="sxs-lookup"><span data-stu-id="b00fd-106">The **Set-AzureRmFirewall** cmdlet updates an Azure Firewall.</span></span>

## <span data-ttu-id="b00fd-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b00fd-107">EXAMPLES</span></span>

### <span data-ttu-id="b00fd-108">1: priorità di aggiornamento di una raccolta di regole applicazione firewall</span><span class="sxs-lookup"><span data-stu-id="b00fd-108">1:  Update priority of a Firewall application rule collection</span></span>
```
$azFw = Get-AzureRmFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$ruleCollection = $azFw.GetApplicationRuleCollectionByName("ruleCollectionName")
$ruleCollection.Priority = 101
Set-AzureRmFirewall -Firewall $azFw
```

<span data-ttu-id="b00fd-109">Questo esempio aggiorna la priorità di una raccolta di regole esistente di un firewall di Azure.</span><span class="sxs-lookup"><span data-stu-id="b00fd-109">This example updates the priority of an existing rule collection of an Azure Firewall.</span></span>
<span data-ttu-id="b00fd-110">Supponendo che il firewall di Azure "AzureFirewall" nel gruppo di risorse "RG" contenga una raccolta di regole dell'applicazione denominata "ruleCollectionName", i comandi descritti sopra cambieranno la priorità della raccolta di regole e aggiorneranno il firewall di Azure in seguito.</span><span class="sxs-lookup"><span data-stu-id="b00fd-110">Assuming Azure Firewall "AzureFirewall" in resource group "rg" contains an application rule collection named "ruleCollectionName", the commands above will change the priority of that rule collection and update the Azure Firewall afterwards.</span></span> <span data-ttu-id="b00fd-111">Senza il comando Set-AzureRmFirewall, tutte le operazioni eseguite sull'oggetto $azFw locale non vengono riflesse nel server.</span><span class="sxs-lookup"><span data-stu-id="b00fd-111">Without the Set-AzureRmFirewall command, all operations performed on the local $azFw object are not reflected on the server.</span></span>

### <span data-ttu-id="b00fd-112">2: creare un firewall di Azure e impostare una raccolta regole applicazione in un secondo momento</span><span class="sxs-lookup"><span data-stu-id="b00fd-112">2:  Create a Azure Firewall and set an application rule collection later</span></span>
```
$azFw = New-AzureRmFirewall -Name "AzureFirewall" -ResourceGroupName "rg" -VirtualNetworkName "vnet-name" -PublicIpName "pip-name"

$rule = New-AzureRmFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$RuleCollection = New-AzureRmFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
$azFw.ApplicationRuleCollections = $RuleCollection

$azFw | Set-AzureRmFirewall
```

<span data-ttu-id="b00fd-113">In questo esempio, un firewall viene creato per primo senza insiemi di regole applicative.</span><span class="sxs-lookup"><span data-stu-id="b00fd-113">In this example, a Firewall is created first without any application rule collections.</span></span> <span data-ttu-id="b00fd-114">In seguito vengono create una regola dell'applicazione e una raccolta regole applicazione, quindi l'oggetto firewall viene modificato in memoria, senza influire sulla configurazione reale nel cloud.</span><span class="sxs-lookup"><span data-stu-id="b00fd-114">Afterwards a Application Rule and Application Rule Collection are created, then the Firewall object is modified in memory, without affecting the real configuration in cloud.</span></span> <span data-ttu-id="b00fd-115">Per il riflesso delle modifiche nel cloud, Set-AzureRmFirewall deve essere chiamato.</span><span class="sxs-lookup"><span data-stu-id="b00fd-115">For changes to be reflected in cloud, Set-AzureRmFirewall must be called.</span></span>

## <span data-ttu-id="b00fd-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b00fd-116">PARAMETERS</span></span>

### <span data-ttu-id="b00fd-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b00fd-117">-AsJob</span></span>
<span data-ttu-id="b00fd-118">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="b00fd-118">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b00fd-119">-AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="b00fd-119">-AzureFirewall</span></span>
<span data-ttu-id="b00fd-120">AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="b00fd-120">The AzureFirewall</span></span>

```yaml
Type: PSAzureFirewall
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b00fd-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b00fd-121">-DefaultProfile</span></span>
<span data-ttu-id="b00fd-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b00fd-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b00fd-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b00fd-123">-Confirm</span></span>
<span data-ttu-id="b00fd-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b00fd-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b00fd-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b00fd-125">-WhatIf</span></span>
<span data-ttu-id="b00fd-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b00fd-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b00fd-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b00fd-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b00fd-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b00fd-128">CommonParameters</span></span>
<span data-ttu-id="b00fd-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b00fd-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b00fd-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b00fd-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b00fd-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b00fd-131">INPUTS</span></span>

### <span data-ttu-id="b00fd-132">PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="b00fd-132">PSAzureFirewall</span></span>
<span data-ttu-id="b00fd-133">Il parametro ' AzureFirewall ' accetta il valore di tipo ' PSAzureFirewall ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="b00fd-133">Parameter 'AzureFirewall' accepts value of type 'PSAzureFirewall' from the pipeline</span></span>

## <span data-ttu-id="b00fd-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b00fd-134">OUTPUTS</span></span>

### <span data-ttu-id="b00fd-135">Microsoft. Azure. Commands. Network. Models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="b00fd-135">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="b00fd-136">Note</span><span class="sxs-lookup"><span data-stu-id="b00fd-136">NOTES</span></span>

## <span data-ttu-id="b00fd-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b00fd-137">RELATED LINKS</span></span>

[<span data-ttu-id="b00fd-138">Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="b00fd-138">Get-AzureRmFirewall</span></span>](./Get-AzureRmFirewall.md)

[<span data-ttu-id="b00fd-139">New-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="b00fd-139">New-AzureRmFirewall</span></span>](./New-AzureRmFirewall.md)

[<span data-ttu-id="b00fd-140">Remove-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="b00fd-140">Remove-AzureRmFirewall</span></span>](./Remove-AzureRmFirewall.md)
