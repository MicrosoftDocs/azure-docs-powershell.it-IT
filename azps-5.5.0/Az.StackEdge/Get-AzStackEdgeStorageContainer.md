---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageContainer.md
ms.openlocfilehash: 0b18183b27f5701036afb74bb85768b48e9492e8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183238"
---
# <span data-ttu-id="18b57-101">Get-AzStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="18b57-101">Get-AzStackEdgeStorageContainer</span></span>

## <span data-ttu-id="18b57-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18b57-102">SYNOPSIS</span></span>
<span data-ttu-id="18b57-103">Ottiene i contenitori per un account di Archiviazione Edge in un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="18b57-103">Gets the containers for an Edge Storage account on a device.</span></span>

## <span data-ttu-id="18b57-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="18b57-104">SYNTAX</span></span>

### <span data-ttu-id="18b57-105">ListParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="18b57-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="18b57-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="18b57-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeStorageContainer [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="18b57-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="18b57-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="18b57-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="18b57-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeStorageContainer [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -EdgeStorageAccountObject <PSStackEdgeStorageAccount> [<CommonParameters>]
```

## <span data-ttu-id="18b57-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="18b57-109">DESCRIPTION</span></span>
<span data-ttu-id="18b57-110">Il cmdlet **Get-AzStackEdgeStorageContainer** ottiene il contenitore di archiviazione per un account di Archiviazione Edge in un dispositivo Stack Edge.</span><span class="sxs-lookup"><span data-stu-id="18b57-110">The **Get-AzStackEdgeStorageContainer** cmdlet gets the storage container for an Edge Storage account on a Stack Edge device.</span></span> <span data-ttu-id="18b57-111">È possibile specificare il nome come parametro nel cmdlet per recuperare i dettagli di uno specifico contenitore di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="18b57-111">You can specify the name as a parameter in the cmdlet to fetch the details of a specific storage container.</span></span> 

## <span data-ttu-id="18b57-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="18b57-112">EXAMPLES</span></span>

### <span data-ttu-id="18b57-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="18b57-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzStackEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1 -Name container1
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
```

### <span data-ttu-id="18b57-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="18b57-114">Example 2</span></span>
```powershell
PS C:\>  Get-AzStackEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container2 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
```

### <span data-ttu-id="18b57-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="18b57-115">Example 3</span></span>
```powershell
PS C:\>  Get-AzStackEdgeDevice -ResourceGroupName resourceGroupName -DeviceName db-edge | Get-AzStackEdgeStorageAccount | Get-AzStackEdgeStorageContainer
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container2 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container4 BlockBlob  Ok     edgestorageaccount2    db-edge    resourceGroupName
container5 BlockBlob  Ok     edgestorageaccount2    db-edge    resourceGroupName
```

## <span data-ttu-id="18b57-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="18b57-116">PARAMETERS</span></span>

### <span data-ttu-id="18b57-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18b57-117">-DefaultProfile</span></span>
<span data-ttu-id="18b57-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="18b57-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18b57-119">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="18b57-119">-DeviceName</span></span>
<span data-ttu-id="18b57-120">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="18b57-120">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18b57-121">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="18b57-121">-EdgeStorageAccountName</span></span>
<span data-ttu-id="18b57-122">Fornisci il nome dell'account EdgeStorageAccount esistente</span><span class="sxs-lookup"><span data-stu-id="18b57-122">Provide existing EdgeStorageAccount's Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18b57-123">-EdgeStorageAccountObject</span><span class="sxs-lookup"><span data-stu-id="18b57-123">-EdgeStorageAccountObject</span></span>
<span data-ttu-id="18b57-124">Fornire un oggetto EdgeStorageAccount esistente</span><span class="sxs-lookup"><span data-stu-id="18b57-124">Provide existing EdgeStorageAccount Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount
Parameter Sets: GetByParentObjectParameterSet
Aliases: EdgeStorageAccount

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="18b57-125">-Name</span><span class="sxs-lookup"><span data-stu-id="18b57-125">-Name</span></span>
<span data-ttu-id="18b57-126">Nome di EdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="18b57-126">Name of the EdgeStorageContainer</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: EdgeStorageContainerName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: EdgeStorageContainerName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18b57-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18b57-127">-ResourceGroupName</span></span>
<span data-ttu-id="18b57-128">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="18b57-128">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18b57-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="18b57-129">-ResourceId</span></span>
<span data-ttu-id="18b57-130">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="18b57-130">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18b57-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18b57-131">CommonParameters</span></span>
<span data-ttu-id="18b57-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18b57-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18b57-133">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="18b57-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18b57-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="18b57-134">INPUTS</span></span>

### <span data-ttu-id="18b57-135">System.String</span><span class="sxs-lookup"><span data-stu-id="18b57-135">System.String</span></span>

### <span data-ttu-id="18b57-136">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="18b57-136">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span></span>

## <span data-ttu-id="18b57-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="18b57-137">OUTPUTS</span></span>

### <span data-ttu-id="18b57-138">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="18b57-138">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span></span>

## <span data-ttu-id="18b57-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="18b57-139">NOTES</span></span>

## <span data-ttu-id="18b57-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="18b57-140">RELATED LINKS</span></span>
