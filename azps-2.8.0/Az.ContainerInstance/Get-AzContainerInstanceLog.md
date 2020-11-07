---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerInstance.dll-Help.xml
Module Name: Az.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerinstance/get-azcontainerinstancelog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Get-AzContainerInstanceLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Get-AzContainerInstanceLog.md
ms.openlocfilehash: f046b9a57f0827977927e31d5009c6276cd89279
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675099"
---
# <span data-ttu-id="9497f-101">Get-AzContainerInstanceLog</span><span class="sxs-lookup"><span data-stu-id="9497f-101">Get-AzContainerInstanceLog</span></span>

## <span data-ttu-id="9497f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9497f-102">SYNOPSIS</span></span>
<span data-ttu-id="9497f-103">Ottenere i log di un'istanza di un contenitore in un gruppo di contenitori.</span><span class="sxs-lookup"><span data-stu-id="9497f-103">Get the logs of a container instance in a container group.</span></span>

## <span data-ttu-id="9497f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9497f-104">SYNTAX</span></span>

### <span data-ttu-id="9497f-105">GetContainerInstanceLogByNamesParamSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9497f-105">GetContainerInstanceLogByNamesParamSet (Default)</span></span>
```
Get-AzContainerInstanceLog [-ResourceGroupName] <String> -ContainerGroupName <String> [-Name <String>]
 [-Tail <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9497f-106">GetContainerInstanceLogByPSContainerGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="9497f-106">GetContainerInstanceLogByPSContainerGroupParamSet</span></span>
```
Get-AzContainerInstanceLog -InputContainerGroup <PSContainerGroup> [-Name <String>] [-Tail <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9497f-107">GetContainerInstanceLogByResourceIdParamSet</span><span class="sxs-lookup"><span data-stu-id="9497f-107">GetContainerInstanceLogByResourceIdParamSet</span></span>
```
Get-AzContainerInstanceLog -ResourceId <String> [-Name <String>] [-Tail <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9497f-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9497f-108">DESCRIPTION</span></span>
<span data-ttu-id="9497f-109">Il cmdlet **Get-AzContainerInstanceLog** recupera i log di un contenitore in un gruppo di contenitori.</span><span class="sxs-lookup"><span data-stu-id="9497f-109">The **Get-AzContainerInstanceLog** cmdlet gets the logs of a container in a container group.</span></span>

## <span data-ttu-id="9497f-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9497f-110">EXAMPLES</span></span>

### <span data-ttu-id="9497f-111">Esempio 1: ottenere il log della coda di un'istanza di contenitore</span><span class="sxs-lookup"><span data-stu-id="9497f-111">Example 1: Get the tail log of a container instance</span></span>
```
PS C:\> Get-AzContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer -Name container1

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="9497f-112">Ottenere il log dal `container1` gruppo contenitore `mycontainer` .</span><span class="sxs-lookup"><span data-stu-id="9497f-112">Get the log from `container1` in container group `mycontainer`.</span></span> <span data-ttu-id="9497f-113">Per impostazione predefinita, verrà restituito il contenuto del log di 4 MB.</span><span class="sxs-lookup"><span data-stu-id="9497f-113">By default, it will return up to 4MB log content.</span></span>

### <span data-ttu-id="9497f-114">Esempio 2: ottenere il log della coda di un'istanza del contenitore con lo stesso nome del gruppo di contenitori</span><span class="sxs-lookup"><span data-stu-id="9497f-114">Example 2: Get the tail log of a container instance that has the same name as the container group</span></span>
```
PS C:\> Get-AzContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="9497f-115">Ottenere il log dal `mycontainer` gruppo contenitore `mycontainer` .</span><span class="sxs-lookup"><span data-stu-id="9497f-115">Get the log from `mycontainer` in container group `mycontainer`.</span></span> <span data-ttu-id="9497f-116">Per impostazione predefinita, verrà restituito il contenuto del log di 4 MB.</span><span class="sxs-lookup"><span data-stu-id="9497f-116">By default, it will return up to 4MB log content.</span></span>

### <span data-ttu-id="9497f-117">Esempio 3: ottenere la coda 2 righe di log di un'istanza di contenitore</span><span class="sxs-lookup"><span data-stu-id="9497f-117">Example 3: Get the tail 2 lines of log of a container instance</span></span>
```
PS C:\> Get-AzContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer -Name container1 -Tail 2

Log line 3.
Log line 4.
```

<span data-ttu-id="9497f-118">Ottenere le righe della coda 2 del log dal `container1` gruppo contenitore `mycontainer` .</span><span class="sxs-lookup"><span data-stu-id="9497f-118">Get the tail 2 lines of log from `container1` in container group `mycontainer`.</span></span>

### <span data-ttu-id="9497f-119">Esempio 4: ottenere il log della coda di un'istanza di un contenitore in un gruppo di contenitori con pipe in</span><span class="sxs-lookup"><span data-stu-id="9497f-119">Example 4: Get the tail log of a container instance in a piped in container group</span></span>
```
PS C:\> Get-AzContainerGroup -ResourceGroupName demo -Name mycontainer | Get-AzContainerInstanceLog

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="9497f-120">Ottenere il log da `mycontainer` in pipe in un gruppo di contenitori `mycontainer` .</span><span class="sxs-lookup"><span data-stu-id="9497f-120">Get the log from `mycontainer` in piped in container group `mycontainer`.</span></span> <span data-ttu-id="9497f-121">Per impostazione predefinita, verrà restituito il contenuto del log di 4 MB.</span><span class="sxs-lookup"><span data-stu-id="9497f-121">By default, it will return up to 4MB log content.</span></span>

## <span data-ttu-id="9497f-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9497f-122">PARAMETERS</span></span>

### <span data-ttu-id="9497f-123">-ContainerGroupName</span><span class="sxs-lookup"><span data-stu-id="9497f-123">-ContainerGroupName</span></span>
<span data-ttu-id="9497f-124">Nome del gruppo di contenitori.</span><span class="sxs-lookup"><span data-stu-id="9497f-124">The container group name.</span></span>

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

### <span data-ttu-id="9497f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9497f-125">-DefaultProfile</span></span>
<span data-ttu-id="9497f-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9497f-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9497f-127">-InputContainerGroup</span><span class="sxs-lookup"><span data-stu-id="9497f-127">-InputContainerGroup</span></span>
<span data-ttu-id="9497f-128">Oggetto gruppo contenitore di input.</span><span class="sxs-lookup"><span data-stu-id="9497f-128">The input container group object.</span></span>

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

### <span data-ttu-id="9497f-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="9497f-129">-Name</span></span>
<span data-ttu-id="9497f-130">Nome dell'istanza del contenitore nel gruppo contenitore.</span><span class="sxs-lookup"><span data-stu-id="9497f-130">The container instance name in the container group.</span></span>
<span data-ttu-id="9497f-131">Impostazione predefinita: uguale al nome del gruppo di contenitori</span><span class="sxs-lookup"><span data-stu-id="9497f-131">Default: the same as the container group name</span></span>

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

### <span data-ttu-id="9497f-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9497f-132">-ResourceGroupName</span></span>
<span data-ttu-id="9497f-133">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9497f-133">The resource group name.</span></span>

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

### <span data-ttu-id="9497f-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9497f-134">-ResourceId</span></span>
<span data-ttu-id="9497f-135">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="9497f-135">The resource id.</span></span>

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

### <span data-ttu-id="9497f-136">-Coda</span><span class="sxs-lookup"><span data-stu-id="9497f-136">-Tail</span></span>
<span data-ttu-id="9497f-137">Numero di righe a cui eseguire il tail log.</span><span class="sxs-lookup"><span data-stu-id="9497f-137">The number of lines to tail the log.</span></span>
<span data-ttu-id="9497f-138">Se non si specifica, il cmdlet restituirà fino a un log di coda di 4 MB</span><span class="sxs-lookup"><span data-stu-id="9497f-138">If not specify, the cmdlet will return up to 4MB tailed log</span></span>

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

### <span data-ttu-id="9497f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9497f-139">CommonParameters</span></span>
<span data-ttu-id="9497f-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9497f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9497f-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9497f-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9497f-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9497f-142">INPUTS</span></span>

### <span data-ttu-id="9497f-143">Microsoft. Azure. Commands. ContainerInstance. Models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="9497f-143">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

### <span data-ttu-id="9497f-144">System. String</span><span class="sxs-lookup"><span data-stu-id="9497f-144">System.String</span></span>

## <span data-ttu-id="9497f-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9497f-145">OUTPUTS</span></span>

### <span data-ttu-id="9497f-146">System. String</span><span class="sxs-lookup"><span data-stu-id="9497f-146">System.String</span></span>

## <span data-ttu-id="9497f-147">Note</span><span class="sxs-lookup"><span data-stu-id="9497f-147">NOTES</span></span>

## <span data-ttu-id="9497f-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9497f-148">RELATED LINKS</span></span>
