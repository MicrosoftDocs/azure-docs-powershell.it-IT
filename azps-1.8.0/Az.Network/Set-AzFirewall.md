---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 40E56EC1-3327-4DFF-8262-E2EEBB5E4447
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewall.md
ms.openlocfilehash: 7937af38c7dd0becd57604a0a7c00e5d1f584e6c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677972"
---
# <span data-ttu-id="3b552-101">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="3b552-101">Set-AzFirewall</span></span>

## <span data-ttu-id="3b552-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3b552-102">SYNOPSIS</span></span>
<span data-ttu-id="3b552-103">Salva un firewall modificato.</span><span class="sxs-lookup"><span data-stu-id="3b552-103">Saves a modified Firewall.</span></span>

## <span data-ttu-id="3b552-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3b552-104">SYNTAX</span></span>

```
Set-AzFirewall -AzureFirewall <PSAzureFirewall> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b552-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3b552-105">DESCRIPTION</span></span>
<span data-ttu-id="3b552-106">Il cmdlet **set-AzFirewall** aggiorna un firewall di Azure.</span><span class="sxs-lookup"><span data-stu-id="3b552-106">The **Set-AzFirewall** cmdlet updates an Azure Firewall.</span></span>

## <span data-ttu-id="3b552-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3b552-107">EXAMPLES</span></span>

### <span data-ttu-id="3b552-108">1: priorità di aggiornamento di una raccolta di regole applicazione firewall</span><span class="sxs-lookup"><span data-stu-id="3b552-108">1:  Update priority of a Firewall application rule collection</span></span>
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$ruleCollection = $azFw.GetApplicationRuleCollectionByName("ruleCollectionName")
$ruleCollection.Priority = 101
Set-AzFirewall -AzureFirewall $azFw
```

<span data-ttu-id="3b552-109">Questo esempio aggiorna la priorità di una raccolta di regole esistente di un firewall di Azure.</span><span class="sxs-lookup"><span data-stu-id="3b552-109">This example updates the priority of an existing rule collection of an Azure Firewall.</span></span>
<span data-ttu-id="3b552-110">Supponendo che il firewall di Azure "AzureFirewall" nel gruppo di risorse "RG" contenga una raccolta di regole dell'applicazione denominata "ruleCollectionName", i comandi descritti sopra cambieranno la priorità della raccolta di regole e aggiorneranno il firewall di Azure in seguito.</span><span class="sxs-lookup"><span data-stu-id="3b552-110">Assuming Azure Firewall "AzureFirewall" in resource group "rg" contains an application rule collection named "ruleCollectionName", the commands above will change the priority of that rule collection and update the Azure Firewall afterwards.</span></span> <span data-ttu-id="3b552-111">Senza il comando Set-AzFirewall, tutte le operazioni eseguite sull'oggetto $azFw locale non vengono riflesse nel server.</span><span class="sxs-lookup"><span data-stu-id="3b552-111">Without the Set-AzFirewall command, all operations performed on the local $azFw object are not reflected on the server.</span></span>

### <span data-ttu-id="3b552-112">2: creare un firewall di Azure e impostare una raccolta regole applicazione in un secondo momento</span><span class="sxs-lookup"><span data-stu-id="3b552-112">2:  Create a Azure Firewall and set an application rule collection later</span></span>
```
$azFw = New-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg" -VirtualNetworkName "vnet-name" -PublicIpName "pip-name"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$RuleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
$azFw.ApplicationRuleCollections = $RuleCollection

$azFw | Set-AzFirewall
```

<span data-ttu-id="3b552-113">In questo esempio, un firewall viene creato per primo senza insiemi di regole applicative.</span><span class="sxs-lookup"><span data-stu-id="3b552-113">In this example, a Firewall is created first without any application rule collections.</span></span> <span data-ttu-id="3b552-114">In seguito vengono create una regola dell'applicazione e una raccolta regole applicazione, quindi l'oggetto firewall viene modificato in memoria, senza influire sulla configurazione reale nel cloud.</span><span class="sxs-lookup"><span data-stu-id="3b552-114">Afterwards a Application Rule and Application Rule Collection are created, then the Firewall object is modified in memory, without affecting the real configuration in cloud.</span></span> <span data-ttu-id="3b552-115">Per il riflesso delle modifiche nel cloud, Set-AzFirewall deve essere chiamato.</span><span class="sxs-lookup"><span data-stu-id="3b552-115">For changes to be reflected in cloud, Set-AzFirewall must be called.</span></span>

### <span data-ttu-id="3b552-116">3: aggiornare la modalità di funzionamento di Intel Threat di Azure firewall</span><span class="sxs-lookup"><span data-stu-id="3b552-116">3:  Update Threat Intel operation mode of Azure Firewall</span></span>
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.ThreatIntelMode = "Deny"
Set-AzFirewall -Firewall $azFw
```

<span data-ttu-id="3b552-117">Questo esempio aggiorna la modalità di funzionamento della minaccia Intel di Azure firewall "AzureFirewall" nel gruppo di risorse "RG".</span><span class="sxs-lookup"><span data-stu-id="3b552-117">This example updates the Threat Intel operation mode of Azure Firewall "AzureFirewall" in resource group "rg".</span></span>
<span data-ttu-id="3b552-118">Senza il comando Set-AzFirewall, tutte le operazioni eseguite sull'oggetto $azFw locale non vengono riflesse nel server.</span><span class="sxs-lookup"><span data-stu-id="3b552-118">Without the Set-AzFirewall command, all operations performed on the local $azFw object are not reflected on the server.</span></span>

## <span data-ttu-id="3b552-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3b552-119">PARAMETERS</span></span>

### <span data-ttu-id="3b552-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3b552-120">-AsJob</span></span>
<span data-ttu-id="3b552-121">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="3b552-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3b552-122">-AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="3b552-122">-AzureFirewall</span></span>
<span data-ttu-id="3b552-123">AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="3b552-123">The AzureFirewall</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewall
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3b552-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b552-124">-DefaultProfile</span></span>
<span data-ttu-id="3b552-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3b552-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3b552-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3b552-126">-Confirm</span></span>
<span data-ttu-id="3b552-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b552-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b552-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b552-128">-WhatIf</span></span>
<span data-ttu-id="3b552-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3b552-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3b552-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3b552-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b552-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b552-131">CommonParameters</span></span>
<span data-ttu-id="3b552-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b552-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b552-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b552-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b552-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3b552-134">INPUTS</span></span>

### <span data-ttu-id="3b552-135">Microsoft. Azure. Commands. Network. Models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="3b552-135">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="3b552-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3b552-136">OUTPUTS</span></span>

### <span data-ttu-id="3b552-137">Microsoft. Azure. Commands. Network. Models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="3b552-137">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="3b552-138">Note</span><span class="sxs-lookup"><span data-stu-id="3b552-138">NOTES</span></span>

## <span data-ttu-id="3b552-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3b552-139">RELATED LINKS</span></span>

[<span data-ttu-id="3b552-140">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="3b552-140">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="3b552-141">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="3b552-141">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="3b552-142">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="3b552-142">Remove-AzFirewall</span></span>](./Remove-AzFirewall.md)
