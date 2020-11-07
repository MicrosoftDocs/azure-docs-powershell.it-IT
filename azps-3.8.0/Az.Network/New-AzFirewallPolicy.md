---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicy.md
ms.openlocfilehash: 5c432224891de6c2fcadc42ae308e9607bc3e432
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93864165"
---
# <span data-ttu-id="9d5c3-101">New-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="9d5c3-101">New-AzFirewallPolicy</span></span>

## <span data-ttu-id="9d5c3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9d5c3-102">SYNOPSIS</span></span>
<span data-ttu-id="9d5c3-103">Crea un nuovo criterio di Azure firewall</span><span class="sxs-lookup"><span data-stu-id="9d5c3-103">Creates a new Azure Firewall Policy</span></span>

## <span data-ttu-id="9d5c3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9d5c3-104">SYNTAX</span></span>

```
New-AzFirewallPolicy -Name <String> -ResourceGroupName <String> -Location <String> [-ThreatIntelMode <String>]
 [-BasePolicy <String>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d5c3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9d5c3-105">DESCRIPTION</span></span>
<span data-ttu-id="9d5c3-106">Il cmdlet **New-AzFirewallPolicy** crea un criterio di Azure firewall.</span><span class="sxs-lookup"><span data-stu-id="9d5c3-106">The **New-AzFirewallPolicy** cmdlet creates an Azure Firewall Policy.</span></span>

## <span data-ttu-id="9d5c3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9d5c3-107">EXAMPLES</span></span>

### <span data-ttu-id="9d5c3-108">1. creare un criterio vuoto</span><span class="sxs-lookup"><span data-stu-id="9d5c3-108">1. Create an empty policy</span></span>
```powershell
PS C:\> New-AzFirewallPolicy -Name fp1 -ResourceGroupName TestRg
```

<span data-ttu-id="9d5c3-109">Questo esempio crea un criterio di Azure firewall</span><span class="sxs-lookup"><span data-stu-id="9d5c3-109">This example creates an azure firewall policy</span></span>

### <span data-ttu-id="9d5c3-110">2. creare un criterio vuoto con la modalità ThreatIntel</span><span class="sxs-lookup"><span data-stu-id="9d5c3-110">2. Create an empty policy with ThreatIntel Mode</span></span>
```powershell
PS C:\> New-AzFirewallPolicy -Name fp1 -ResourceGroupName TestRg -ThreatIntelMode "Deny"
```

<span data-ttu-id="9d5c3-111">Questo esempio crea un criterio di Azure Firewall con una modalità Intel per le minacce</span><span class="sxs-lookup"><span data-stu-id="9d5c3-111">This example creates an azure firewall policy with a threat intel mode</span></span>

## <span data-ttu-id="9d5c3-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9d5c3-112">PARAMETERS</span></span>

### <span data-ttu-id="9d5c3-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9d5c3-113">-AsJob</span></span>
<span data-ttu-id="9d5c3-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="9d5c3-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9d5c3-115">-BasePolicy</span><span class="sxs-lookup"><span data-stu-id="9d5c3-115">-BasePolicy</span></span>
<span data-ttu-id="9d5c3-116">Modalità operativa per Threat Intelligence.</span><span class="sxs-lookup"><span data-stu-id="9d5c3-116">The operation mode for Threat Intelligence.</span></span>

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

### <span data-ttu-id="9d5c3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d5c3-117">-DefaultProfile</span></span>
<span data-ttu-id="9d5c3-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9d5c3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9d5c3-119">-Force</span><span class="sxs-lookup"><span data-stu-id="9d5c3-119">-Force</span></span>
<span data-ttu-id="9d5c3-120">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="9d5c3-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="9d5c3-121">-Posizione</span><span class="sxs-lookup"><span data-stu-id="9d5c3-121">-Location</span></span>
<span data-ttu-id="9d5c3-122">posizione.</span><span class="sxs-lookup"><span data-stu-id="9d5c3-122">location.</span></span>

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

### <span data-ttu-id="9d5c3-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="9d5c3-123">-Name</span></span>
<span data-ttu-id="9d5c3-124">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="9d5c3-124">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d5c3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d5c3-125">-ResourceGroupName</span></span>
<span data-ttu-id="9d5c3-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9d5c3-126">The resource group name.</span></span>

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

### <span data-ttu-id="9d5c3-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="9d5c3-127">-Tag</span></span>
<span data-ttu-id="9d5c3-128">Hashtable che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="9d5c3-128">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d5c3-129">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="9d5c3-129">-ThreatIntelMode</span></span>
<span data-ttu-id="9d5c3-130">Modalità operativa per Threat Intelligence.</span><span class="sxs-lookup"><span data-stu-id="9d5c3-130">The operation mode for Threat Intelligence.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Alert, Deny, Off

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d5c3-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9d5c3-131">-Confirm</span></span>
<span data-ttu-id="9d5c3-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d5c3-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d5c3-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d5c3-133">-WhatIf</span></span>
<span data-ttu-id="9d5c3-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9d5c3-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d5c3-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9d5c3-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d5c3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d5c3-136">CommonParameters</span></span>
<span data-ttu-id="9d5c3-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d5c3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d5c3-138">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9d5c3-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d5c3-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9d5c3-139">INPUTS</span></span>

### <span data-ttu-id="9d5c3-140">System. String</span><span class="sxs-lookup"><span data-stu-id="9d5c3-140">System.String</span></span>

### <span data-ttu-id="9d5c3-141">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="9d5c3-141">System.Collections.Hashtable</span></span>

## <span data-ttu-id="9d5c3-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9d5c3-142">OUTPUTS</span></span>

### <span data-ttu-id="9d5c3-143">Microsoft. Azure. Commands. Network. Models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="9d5c3-143">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="9d5c3-144">Note</span><span class="sxs-lookup"><span data-stu-id="9d5c3-144">NOTES</span></span>

## <span data-ttu-id="9d5c3-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9d5c3-145">RELATED LINKS</span></span>
