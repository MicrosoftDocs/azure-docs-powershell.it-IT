---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerInstance.dll-Help.xml
Module Name: Az.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerinstance/get-azcontainerinstancelog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Get-AzContainerInstanceLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Get-AzContainerInstanceLog.md
ms.openlocfilehash: d279e5c08b43640d629e4146faf306d0e85482a8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019128"
---
# <span data-ttu-id="a70fd-101">Get-AzContainerInstanceLog</span><span class="sxs-lookup"><span data-stu-id="a70fd-101">Get-AzContainerInstanceLog</span></span>

## <span data-ttu-id="a70fd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a70fd-102">SYNOPSIS</span></span>
<span data-ttu-id="a70fd-103">Ottenere i log di un'istanza di un contenitore in un gruppo di contenitori.</span><span class="sxs-lookup"><span data-stu-id="a70fd-103">Get the logs of a container instance in a container group.</span></span>

## <span data-ttu-id="a70fd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a70fd-104">SYNTAX</span></span>

### <span data-ttu-id="a70fd-105">GetContainerInstanceLogByNamesParamSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a70fd-105">GetContainerInstanceLogByNamesParamSet (Default)</span></span>
```
Get-AzContainerInstanceLog [-ResourceGroupName] <String> -ContainerGroupName <String> [-Name <String>]
 [-Tail <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a70fd-106">GetContainerInstanceLogByPSContainerGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="a70fd-106">GetContainerInstanceLogByPSContainerGroupParamSet</span></span>
```
Get-AzContainerInstanceLog -InputContainerGroup <PSContainerGroup> [-Name <String>] [-Tail <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a70fd-107">GetContainerInstanceLogByResourceIdParamSet</span><span class="sxs-lookup"><span data-stu-id="a70fd-107">GetContainerInstanceLogByResourceIdParamSet</span></span>
```
Get-AzContainerInstanceLog -ResourceId <String> [-Name <String>] [-Tail <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a70fd-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a70fd-108">DESCRIPTION</span></span>
<span data-ttu-id="a70fd-109">Il cmdlet **Get-AzContainerInstanceLog** recupera i log di un contenitore in un gruppo di contenitori.</span><span class="sxs-lookup"><span data-stu-id="a70fd-109">The **Get-AzContainerInstanceLog** cmdlet gets the logs of a container in a container group.</span></span>

## <span data-ttu-id="a70fd-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a70fd-110">EXAMPLES</span></span>

### <span data-ttu-id="a70fd-111">Esempio 1: ottenere il log della coda di un'istanza di contenitore</span><span class="sxs-lookup"><span data-stu-id="a70fd-111">Example 1: Get the tail log of a container instance</span></span>
```
PS C:\> Get-AzContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer -Name container1

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="a70fd-112">Ottenere il log dal `container1` gruppo contenitore `mycontainer` .</span><span class="sxs-lookup"><span data-stu-id="a70fd-112">Get the log from `container1` in container group `mycontainer`.</span></span> <span data-ttu-id="a70fd-113">Per impostazione predefinita, verrà restituito il contenuto del log di 4 MB.</span><span class="sxs-lookup"><span data-stu-id="a70fd-113">By default, it will return up to 4MB log content.</span></span>

### <span data-ttu-id="a70fd-114">Esempio 2: ottenere il log della coda di un'istanza del contenitore con lo stesso nome del gruppo di contenitori</span><span class="sxs-lookup"><span data-stu-id="a70fd-114">Example 2: Get the tail log of a container instance that has the same name as the container group</span></span>
```
PS C:\> Get-AzContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="a70fd-115">Ottenere il log dal `mycontainer` gruppo contenitore `mycontainer` .</span><span class="sxs-lookup"><span data-stu-id="a70fd-115">Get the log from `mycontainer` in container group `mycontainer`.</span></span> <span data-ttu-id="a70fd-116">Per impostazione predefinita, verrà restituito il contenuto del log di 4 MB.</span><span class="sxs-lookup"><span data-stu-id="a70fd-116">By default, it will return up to 4MB log content.</span></span>

### <span data-ttu-id="a70fd-117">Esempio 3: ottenere la coda 2 righe di log di un'istanza di contenitore</span><span class="sxs-lookup"><span data-stu-id="a70fd-117">Example 3: Get the tail 2 lines of log of a container instance</span></span>
```
PS C:\> Get-AzContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer -Name container1 -Tail 2

Log line 3.
Log line 4.
```

<span data-ttu-id="a70fd-118">Ottenere le righe della coda 2 del log dal `container1` gruppo contenitore `mycontainer` .</span><span class="sxs-lookup"><span data-stu-id="a70fd-118">Get the tail 2 lines of log from `container1` in container group `mycontainer`.</span></span>

### <span data-ttu-id="a70fd-119">Esempio 4: ottenere il log della coda di un'istanza di un contenitore in un gruppo di contenitori con pipe in</span><span class="sxs-lookup"><span data-stu-id="a70fd-119">Example 4: Get the tail log of a container instance in a piped in container group</span></span>
```
PS C:\> Get-AzContainerGroup -ResourceGroupName demo -Name mycontainer | Get-AzContainerInstanceLog

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="a70fd-120">Ottenere il log da `mycontainer` in pipe in un gruppo di contenitori `mycontainer` .</span><span class="sxs-lookup"><span data-stu-id="a70fd-120">Get the log from `mycontainer` in piped in container group `mycontainer`.</span></span> <span data-ttu-id="a70fd-121">Per impostazione predefinita, verrà restituito il contenuto del log di 4 MB.</span><span class="sxs-lookup"><span data-stu-id="a70fd-121">By default, it will return up to 4MB log content.</span></span>

## <span data-ttu-id="a70fd-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a70fd-122">PARAMETERS</span></span>

### <span data-ttu-id="a70fd-123">-ContainerGroupName</span><span class="sxs-lookup"><span data-stu-id="a70fd-123">-ContainerGroupName</span></span>
<span data-ttu-id="a70fd-124">Nome del gruppo di contenitori.</span><span class="sxs-lookup"><span data-stu-id="a70fd-124">The container group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetContainerInstanceLogByNamesParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a70fd-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a70fd-125">-DefaultProfile</span></span>
<span data-ttu-id="a70fd-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a70fd-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a70fd-127">-InputContainerGroup</span><span class="sxs-lookup"><span data-stu-id="a70fd-127">-InputContainerGroup</span></span>
<span data-ttu-id="a70fd-128">Oggetto gruppo contenitore di input.</span><span class="sxs-lookup"><span data-stu-id="a70fd-128">The input container group object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup
Parameter Sets: GetContainerInstanceLogByPSContainerGroupParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a70fd-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="a70fd-129">-Name</span></span>
<span data-ttu-id="a70fd-130">Nome dell'istanza del contenitore nel gruppo contenitore.</span><span class="sxs-lookup"><span data-stu-id="a70fd-130">The container instance name in the container group.</span></span>
<span data-ttu-id="a70fd-131">Impostazione predefinita: uguale al nome del gruppo di contenitori</span><span class="sxs-lookup"><span data-stu-id="a70fd-131">Default: the same as the container group name</span></span>

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

### <span data-ttu-id="a70fd-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a70fd-132">-ResourceGroupName</span></span>
<span data-ttu-id="a70fd-133">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a70fd-133">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetContainerInstanceLogByNamesParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a70fd-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a70fd-134">-ResourceId</span></span>
<span data-ttu-id="a70fd-135">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="a70fd-135">The resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: GetContainerInstanceLogByResourceIdParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a70fd-136">-Coda</span><span class="sxs-lookup"><span data-stu-id="a70fd-136">-Tail</span></span>
<span data-ttu-id="a70fd-137">Numero di righe a cui eseguire il tail log.</span><span class="sxs-lookup"><span data-stu-id="a70fd-137">The number of lines to tail the log.</span></span>
<span data-ttu-id="a70fd-138">Se non si specifica, il cmdlet restituirà fino a un log di coda di 4 MB</span><span class="sxs-lookup"><span data-stu-id="a70fd-138">If not specify, the cmdlet will return up to 4MB tailed log</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a70fd-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a70fd-139">CommonParameters</span></span>
<span data-ttu-id="a70fd-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a70fd-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a70fd-141">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a70fd-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a70fd-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a70fd-142">INPUTS</span></span>

### <span data-ttu-id="a70fd-143">Microsoft. Azure. Commands. ContainerInstance. Models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="a70fd-143">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

### <span data-ttu-id="a70fd-144">System. String</span><span class="sxs-lookup"><span data-stu-id="a70fd-144">System.String</span></span>

## <span data-ttu-id="a70fd-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a70fd-145">OUTPUTS</span></span>

### <span data-ttu-id="a70fd-146">System. String</span><span class="sxs-lookup"><span data-stu-id="a70fd-146">System.String</span></span>

## <span data-ttu-id="a70fd-147">Note</span><span class="sxs-lookup"><span data-stu-id="a70fd-147">NOTES</span></span>

## <span data-ttu-id="a70fd-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a70fd-148">RELATED LINKS</span></span>
