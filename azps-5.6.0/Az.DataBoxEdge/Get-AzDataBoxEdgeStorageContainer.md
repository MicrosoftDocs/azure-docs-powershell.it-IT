---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/get-azdataboxedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageContainer.md
ms.openlocfilehash: fb60583922fd01d2f3a472525f3210b070fb5935
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001677"
---
# <span data-ttu-id="7b5b0-101">Get-AzDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="7b5b0-101">Get-AzDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="7b5b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b5b0-102">SYNOPSIS</span></span>
<span data-ttu-id="7b5b0-103">Ottiene i contenitori per un account di Archiviazione Edge in un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7b5b0-103">Gets the containers for an Edge Storage account on a device.</span></span>

## <span data-ttu-id="7b5b0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7b5b0-104">SYNTAX</span></span>

### <span data-ttu-id="7b5b0-105">ListParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7b5b0-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7b5b0-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7b5b0-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageContainer [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7b5b0-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7b5b0-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7b5b0-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7b5b0-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageContainer [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -EdgeStorageAccountObject <PSDataBoxEdgeStorageAccount> [<CommonParameters>]
```

## <span data-ttu-id="7b5b0-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7b5b0-109">DESCRIPTION</span></span>
<span data-ttu-id="7b5b0-110">Il cmdlet **Get-AzDataBoxEdgeStorageContainer** ottiene il contenitore di archiviazione per un account di Archiviazione Edge in un dispositivo Edge di Data Box.</span><span class="sxs-lookup"><span data-stu-id="7b5b0-110">The **Get-AzDataBoxEdgeStorageContainer** cmdlet gets the storage container for an Edge Storage account on a Data Box Edge device.</span></span> <span data-ttu-id="7b5b0-111">È possibile specificare il nome come parametro nel cmdlet per recuperare i dettagli di uno specifico contenitore di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="7b5b0-111">You can specify the name as a parameter in the cmdlet to fetch the details of a specific storage container.</span></span> 

## <span data-ttu-id="7b5b0-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7b5b0-112">EXAMPLES</span></span>

### <span data-ttu-id="7b5b0-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7b5b0-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1 -Name container1
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
```

### <span data-ttu-id="7b5b0-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="7b5b0-114">Example 2</span></span>
```powershell
PS C:\>  Get-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container2 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
```

### <span data-ttu-id="7b5b0-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="7b5b0-115">Example 3</span></span>
```powershell
PS C:\>  Get-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -DeviceName db-edge | Get-AzDataBoxEdgeStorageAccount | Get-AzDataBoxEdgeStorageContainer
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container2 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container4 BlockBlob  Ok     edgestorageaccount2    db-edge    resourceGroupName
container5 BlockBlob  Ok     edgestorageaccount2    db-edge    resourceGroupName
```

## <span data-ttu-id="7b5b0-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7b5b0-116">PARAMETERS</span></span>

### <span data-ttu-id="7b5b0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b5b0-117">-DefaultProfile</span></span>
<span data-ttu-id="7b5b0-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7b5b0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b5b0-119">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="7b5b0-119">-DeviceName</span></span>
<span data-ttu-id="7b5b0-120">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="7b5b0-120">Device Name</span></span>

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

### <span data-ttu-id="7b5b0-121">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="7b5b0-121">-EdgeStorageAccountName</span></span>
<span data-ttu-id="7b5b0-122">Fornisci il nome dell'account EdgeStorageAccount esistente</span><span class="sxs-lookup"><span data-stu-id="7b5b0-122">Provide existing EdgeStorageAccount's Name</span></span>

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

### <span data-ttu-id="7b5b0-123">-EdgeStorageAccountObject</span><span class="sxs-lookup"><span data-stu-id="7b5b0-123">-EdgeStorageAccountObject</span></span>
<span data-ttu-id="7b5b0-124">Fornire l'oggetto EdgeStorageAccount esistente</span><span class="sxs-lookup"><span data-stu-id="7b5b0-124">Provide existing EdgeStorageAccount Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7b5b0-125">-Name</span><span class="sxs-lookup"><span data-stu-id="7b5b0-125">-Name</span></span>
<span data-ttu-id="7b5b0-126">Nome di EdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="7b5b0-126">Name of the EdgeStorageContainer</span></span>

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

### <span data-ttu-id="7b5b0-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b5b0-127">-ResourceGroupName</span></span>
<span data-ttu-id="7b5b0-128">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="7b5b0-128">Resource Group Name</span></span>

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

### <span data-ttu-id="7b5b0-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7b5b0-129">-ResourceId</span></span>
<span data-ttu-id="7b5b0-130">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="7b5b0-130">Azure ResourceId</span></span>

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

### <span data-ttu-id="7b5b0-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b5b0-131">CommonParameters</span></span>
<span data-ttu-id="7b5b0-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b5b0-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b5b0-133">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7b5b0-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b5b0-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="7b5b0-134">INPUTS</span></span>

### <span data-ttu-id="7b5b0-135">System.String</span><span class="sxs-lookup"><span data-stu-id="7b5b0-135">System.String</span></span>

### <span data-ttu-id="7b5b0-136">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7b5b0-136">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="7b5b0-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7b5b0-137">OUTPUTS</span></span>

### <span data-ttu-id="7b5b0-138">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="7b5b0-138">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="7b5b0-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="7b5b0-139">NOTES</span></span>

## <span data-ttu-id="7b5b0-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7b5b0-140">RELATED LINKS</span></span>
