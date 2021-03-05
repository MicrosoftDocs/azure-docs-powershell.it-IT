---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerInstance.dll-Help.xml
Module Name: Az.ContainerInstance
online version: https://docs.microsoft.com/powershell/module/az.containerinstance/get-azcontainergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Get-AzContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Get-AzContainerGroup.md
ms.openlocfilehash: 65e6fbaa61285f946726fee9dce2261c998931cd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012270"
---
# <span data-ttu-id="9343e-101">Get-AzContainerGroup</span><span class="sxs-lookup"><span data-stu-id="9343e-101">Get-AzContainerGroup</span></span>

## <span data-ttu-id="9343e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9343e-102">SYNOPSIS</span></span>
<span data-ttu-id="9343e-103">Recupera i gruppi di contenitori.</span><span class="sxs-lookup"><span data-stu-id="9343e-103">Gets container groups.</span></span>

## <span data-ttu-id="9343e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9343e-104">SYNTAX</span></span>

### <span data-ttu-id="9343e-105">ListContainerGroupParamSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9343e-105">ListContainerGroupParamSet (Default)</span></span>
```
Get-AzContainerGroup [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9343e-106">GetContainerGroupInResourceGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="9343e-106">GetContainerGroupInResourceGroupParamSet</span></span>
```
Get-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9343e-107">GetContainerGroupByResourceIdParamSet</span><span class="sxs-lookup"><span data-stu-id="9343e-107">GetContainerGroupByResourceIdParamSet</span></span>
```
Get-AzContainerGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9343e-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9343e-108">DESCRIPTION</span></span>
<span data-ttu-id="9343e-109">Il cmdlet **Get-AzContainerGroup** ottiene un gruppo di contenitore specificato o tutti i gruppi di contenitori in un gruppo di risorse o nella sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="9343e-109">The **Get-AzContainerGroup** cmdlet gets a specified container group or all the container groups in a resource group or the subscription.</span></span>

## <span data-ttu-id="9343e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9343e-110">EXAMPLES</span></span>

### <span data-ttu-id="9343e-111">Esempio 1: Ottiene un gruppo di contenitore specificato</span><span class="sxs-lookup"><span data-stu-id="9343e-111">Example 1: Gets a specified container group</span></span>
```
PS C:\> Get-AzContainerGroup -ResourceGroupName demo -Name mycontainer

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Succeeded
Containers               : {mycontainer}
ImageRegistryCredentials :
RestartPolicy            :
IpAddress                : 13.88.10.240
Ports                    : {8000}
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
```

<span data-ttu-id="9343e-112">Il comando ottiene il gruppo di contenitori specificato.</span><span class="sxs-lookup"><span data-stu-id="9343e-112">The command gets the specified container group.</span></span>

### <span data-ttu-id="9343e-113">Esempio 2: Ottiene gruppi di contenitori in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="9343e-113">Example 2: Gets container groups in a resource group</span></span>
```
PS C:\> Get-AzContainerGroup -ResourceGroupName demo

ResourceGroupName Name                     Location   OsType  Image                         IP                   Resources        ProvisioningState
----------------- ----                     --------   ------  -----                         --                   ---------        -----------------
demo              container1               west us    Linux   alpine:latest                 40.83.144.50:8002    1 cores/1 gb             Succeeded
demo              container2               west us    Linux   alpine:latest                 104.42.228.253:8001  1 cores/1 gb             Succeeded
```

<span data-ttu-id="9343e-114">Il comando ottiene i gruppi di contenitori nel gruppo di `demo` risorse.</span><span class="sxs-lookup"><span data-stu-id="9343e-114">The command gets the container groups in the resource group `demo`.</span></span>

### <span data-ttu-id="9343e-115">Esempio 3: Ottiene i gruppi di contenitori nella sottoscrizione corrente</span><span class="sxs-lookup"><span data-stu-id="9343e-115">Example 3: Gets container groups in the current subscription</span></span>
```
PS C:\> Get-AzContainerGroup

ResourceGroupName Name                     Location   OsType  Image                         IP                   Resources        ProvisioningState
----------------- ----                     --------   ------  -----                         --                   ---------        -----------------
demo1             container1               west us    Linux   alpine:latest                 40.83.144.50:8002    1 cores/1 gb             Succeeded
demo2             container2               west us    Linux   alpine:latest                 104.42.228.253:8001  1 cores/1 gb             Succeeded
```

<span data-ttu-id="9343e-116">Il comando recupera i gruppi di contenitori nella sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="9343e-116">The command gets the container groups in the current subscription.</span></span>

### <span data-ttu-id="9343e-117">Esempio 4: ottiene i gruppi di contenitori usando l'ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="9343e-117">Example 4: Gets container groups using resource Id.</span></span>
```
PS C:\> Find-AzResource -ResourceGroupEquals demo -ResourceNameEquals mycontainer | Get-AzContainerGroup

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Succeeded
Containers               : {mycontainer}
ImageRegistryCredentials :
RestartPolicy            :
IpAddress                : 13.88.10.240
Ports                    : {8000}
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
```

<span data-ttu-id="9343e-118">Il comando ottiene il gruppo di contenitori con l'ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="9343e-118">The command gets the container group with the resource Id.</span></span>

## <span data-ttu-id="9343e-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9343e-119">PARAMETERS</span></span>

### <span data-ttu-id="9343e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9343e-120">-DefaultProfile</span></span>
<span data-ttu-id="9343e-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9343e-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9343e-122">-Name</span><span class="sxs-lookup"><span data-stu-id="9343e-122">-Name</span></span>
<span data-ttu-id="9343e-123">Nome del gruppo di contenitori.</span><span class="sxs-lookup"><span data-stu-id="9343e-123">The container group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetContainerGroupInResourceGroupParamSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9343e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9343e-124">-ResourceGroupName</span></span>
<span data-ttu-id="9343e-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9343e-125">The resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListContainerGroupParamSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetContainerGroupInResourceGroupParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9343e-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9343e-126">-ResourceId</span></span>
<span data-ttu-id="9343e-127">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="9343e-127">The resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: GetContainerGroupByResourceIdParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9343e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9343e-128">CommonParameters</span></span>
<span data-ttu-id="9343e-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9343e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9343e-130">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9343e-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9343e-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="9343e-131">INPUTS</span></span>

### <span data-ttu-id="9343e-132">System.String</span><span class="sxs-lookup"><span data-stu-id="9343e-132">System.String</span></span>

## <span data-ttu-id="9343e-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9343e-133">OUTPUTS</span></span>

### <span data-ttu-id="9343e-134">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="9343e-134">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="9343e-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="9343e-135">NOTES</span></span>

## <span data-ttu-id="9343e-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9343e-136">RELATED LINKS</span></span>
