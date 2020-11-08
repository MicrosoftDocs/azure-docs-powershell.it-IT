---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityTopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityTopology.md
ms.openlocfilehash: ef984a1cbb1cf922ddc931a7924a5d39ba6c6a0b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200996"
---
# <span data-ttu-id="d6287-101">Get-AzSecurityTopology</span><span class="sxs-lookup"><span data-stu-id="d6287-101">Get-AzSecurityTopology</span></span>

## <span data-ttu-id="d6287-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d6287-102">SYNOPSIS</span></span>
<span data-ttu-id="d6287-103">Ottiene un elenco delle topologie di sicurezza in un abbonamento</span><span class="sxs-lookup"><span data-stu-id="d6287-103">Gets a list of Security Topologies on a subscription</span></span>

## <span data-ttu-id="d6287-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d6287-104">SYNTAX</span></span>

### <span data-ttu-id="d6287-105">SubscriptionScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d6287-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityTopology [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6287-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="d6287-106">ResourceGroupLevelResource</span></span>
```
Get-AzSecurityTopology -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6287-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="d6287-107">ResourceId</span></span>
```
Get-AzSecurityTopology -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d6287-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d6287-108">DESCRIPTION</span></span>
<span data-ttu-id="d6287-109">Le topologie di sicurezza vengono scoperte automaticamente da Azure Security Center, usare questo cmdlet per visualizzare le topologie di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="d6287-109">Security Topologies are automatically discovered by Azure Security Center, use this cmdlet to view security topologies.</span></span>

## <span data-ttu-id="d6287-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d6287-110">EXAMPLES</span></span>

### <span data-ttu-id="d6287-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d6287-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityTopology
Id: /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/topologies/virtualMachines
Name:   virtualMachines
Type:   Microsoft.Security/locations/topologies
CalculatedDateTime: 03-Jun-20 3:03:48 PM
TopologyResources:  /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myvm
```

<span data-ttu-id="d6287-112">Visualizzare tutte le topologie di sicurezza in un abbonamento</span><span class="sxs-lookup"><span data-stu-id="d6287-112">View all security topologies in a subscription</span></span>

### <span data-ttu-id="d6287-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="d6287-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSecurityTopology -ResourceGroupName "myService1" -Location "centralus" -Name "virtualMachines"
Id: /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/topologies/virtualMachines
Name:   virtualMachines
Type:   Microsoft.Security/locations/topologies
CalculatedDateTime: 03-Jun-20 3:03:48 PM
TopologyResources:  /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myvm
```

<span data-ttu-id="d6287-114">Ottenere una topologia di sicurezza specifica</span><span class="sxs-lookup"><span data-stu-id="d6287-114">Get a specific security topologies</span></span>

## <span data-ttu-id="d6287-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d6287-115">PARAMETERS</span></span>

### <span data-ttu-id="d6287-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6287-116">-DefaultProfile</span></span>
<span data-ttu-id="d6287-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d6287-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6287-118">-Posizione</span><span class="sxs-lookup"><span data-stu-id="d6287-118">-Location</span></span>
<span data-ttu-id="d6287-119">Posizione.</span><span class="sxs-lookup"><span data-stu-id="d6287-119">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6287-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="d6287-120">-Name</span></span>
<span data-ttu-id="d6287-121">Nome risorsa.</span><span class="sxs-lookup"><span data-stu-id="d6287-121">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6287-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6287-122">-ResourceGroupName</span></span>
<span data-ttu-id="d6287-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d6287-123">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6287-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d6287-124">-ResourceId</span></span>
<span data-ttu-id="d6287-125">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="d6287-125">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6287-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6287-126">CommonParameters</span></span>
<span data-ttu-id="d6287-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6287-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6287-128">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6287-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6287-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d6287-129">INPUTS</span></span>

### <span data-ttu-id="d6287-130">System. String</span><span class="sxs-lookup"><span data-stu-id="d6287-130">System.String</span></span>

## <span data-ttu-id="d6287-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d6287-131">OUTPUTS</span></span>

### <span data-ttu-id="d6287-132">Microsoft. Azure. Commands. Security. Models. topologia. PSSecurityTopologies</span><span class="sxs-lookup"><span data-stu-id="d6287-132">Microsoft.Azure.Commands.Security.Models.Topology.PSSecurityTopologies</span></span>

## <span data-ttu-id="d6287-133">Note</span><span class="sxs-lookup"><span data-stu-id="d6287-133">NOTES</span></span>

## <span data-ttu-id="d6287-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d6287-134">RELATED LINKS</span></span>
