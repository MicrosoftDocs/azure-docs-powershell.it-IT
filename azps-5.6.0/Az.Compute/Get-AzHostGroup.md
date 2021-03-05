---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azhostgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzHostGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzHostGroup.md
ms.openlocfilehash: 1b33803ff3a33897d46519952db99ceda1b12c99
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991520"
---
# <span data-ttu-id="9eba2-101">Get-AzHostGroup</span><span class="sxs-lookup"><span data-stu-id="9eba2-101">Get-AzHostGroup</span></span>

## <span data-ttu-id="9eba2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9eba2-102">SYNOPSIS</span></span>
<span data-ttu-id="9eba2-103">Ottenere o elencare gli ospiti.</span><span class="sxs-lookup"><span data-stu-id="9eba2-103">Get or list hosts.</span></span>

## <span data-ttu-id="9eba2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9eba2-104">SYNTAX</span></span>

### <span data-ttu-id="9eba2-105">DefaultParameter (Default)</span><span class="sxs-lookup"><span data-stu-id="9eba2-105">DefaultParameter (Default)</span></span>
```
Get-AzHostGroup [[-ResourceGroupName] <String>] [[-Name] <String>] [-InstanceView]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9eba2-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="9eba2-106">ResourceIdParameter</span></span>
```
Get-AzHostGroup [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9eba2-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9eba2-107">DESCRIPTION</span></span>
<span data-ttu-id="9eba2-108">Questo cmdlet otterrà un gruppo host.</span><span class="sxs-lookup"><span data-stu-id="9eba2-108">This cmdlet will get a host group.</span></span>
<span data-ttu-id="9eba2-109">Se non viene assegnato un nome a un gruppo host, questo cmdlet elenca anche tutti i gruppi host in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9eba2-109">This cmdlet also lists all host groups in a resource group if a host group name is not given.</span></span>
<span data-ttu-id="9eba2-110">Questo cmdlet elenca anche tutti i gruppi host in una sottoscrizione se non viene assegnato né il nome del gruppo host né il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9eba2-110">This cmdlet also lists all host groups in a subscription if neither host group name nor resource group name is given.</span></span>

## <span data-ttu-id="9eba2-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9eba2-111">EXAMPLES</span></span>

### <span data-ttu-id="9eba2-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9eba2-112">Example 1</span></span>
```
PS C:\> Get-AzHostGroup -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName

ResourceGroupName        : myrg01
PlatformFaultDomainCount : 2
Hosts                    : {/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/hostGroups/myhostgroup01/hosts/myhost01}
Zones                    : {1}
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/hostGroups/myhostgroup01
Name                     : myhostgroup01
Location                 : eastus
Tags                     : {[key1, val1]}
```

<span data-ttu-id="9eba2-113">Questo comando restituisce un gruppo host.</span><span class="sxs-lookup"><span data-stu-id="9eba2-113">This command returns a host group.</span></span>

### <span data-ttu-id="9eba2-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="9eba2-114">Example 2</span></span>
```
PS C:\> Get-AzHostGroup -ResourceGroupName $resourceGroupName

ResourceGroupName                   Name Location           Tags FDCount
-----------------                   ---- --------           ---- -------
myrg01                     myhostgroup01   eastus {[key1, val1]}       1
myrg01                     myhostgroup02   eastus {[key1, val1]}       2
```

<span data-ttu-id="9eba2-115">Questo comando restituisce tutti i gruppi host nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="9eba2-115">This command returns all host groups in the given resource group.</span></span>

### <span data-ttu-id="9eba2-116">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="9eba2-116">Example 3</span></span>
```
PS C:\> Get-AzHostGroup

ResourceGroupName                   Name Location           Tags FDCount
-----------------                   ---- --------           ---- -------
myrg01                     myhostgroup01   eastus {[key1, val1]}       1
myrg01                     myhostgroup02   eastus {[key1, val1]}       2
myrg02                     myhostgroup03   eastus {[key1, val1]}       2
```

<span data-ttu-id="9eba2-117">Questo comando restituisce tutti i gruppi host della sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="9eba2-117">This command returns all host groups in the subscription.</span></span>

## <span data-ttu-id="9eba2-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9eba2-118">PARAMETERS</span></span>

### <span data-ttu-id="9eba2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9eba2-119">-DefaultProfile</span></span>
<span data-ttu-id="9eba2-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9eba2-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9eba2-121">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="9eba2-121">-InstanceView</span></span>
<span data-ttu-id="9eba2-122">Espandere l'oggetto restituito per elencare anche le visualizzazioni dell'istanza dell'host.</span><span class="sxs-lookup"><span data-stu-id="9eba2-122">Expand the returned object to also list the host's instance views.</span></span> 

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultParameter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9eba2-123">-Name</span><span class="sxs-lookup"><span data-stu-id="9eba2-123">-Name</span></span>
<span data-ttu-id="9eba2-124">Nome del gruppo host.</span><span class="sxs-lookup"><span data-stu-id="9eba2-124">The name of the host group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: HostGroupName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9eba2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9eba2-125">-ResourceGroupName</span></span>
<span data-ttu-id="9eba2-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9eba2-126">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9eba2-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9eba2-127">-ResourceId</span></span>
<span data-ttu-id="9eba2-128">ID della risorsa.</span><span class="sxs-lookup"><span data-stu-id="9eba2-128">The ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9eba2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9eba2-129">CommonParameters</span></span>
<span data-ttu-id="9eba2-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9eba2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9eba2-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9eba2-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9eba2-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="9eba2-132">INPUTS</span></span>

### <span data-ttu-id="9eba2-133">System.String</span><span class="sxs-lookup"><span data-stu-id="9eba2-133">System.String</span></span>

## <span data-ttu-id="9eba2-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9eba2-134">OUTPUTS</span></span>

### <span data-ttu-id="9eba2-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span><span class="sxs-lookup"><span data-stu-id="9eba2-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span></span>

## <span data-ttu-id="9eba2-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="9eba2-136">NOTES</span></span>

## <span data-ttu-id="9eba2-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9eba2-137">RELATED LINKS</span></span>
