---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeShare.md
ms.openlocfilehash: 6a20f81644827c84ee1ce215ad2e87268650caf9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98477267"
---
# <span data-ttu-id="4cf74-101">Get-AzDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="4cf74-101">Get-AzDataBoxEdgeShare</span></span>

## <span data-ttu-id="4cf74-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4cf74-102">SYNOPSIS</span></span>
<span data-ttu-id="4cf74-103">Ottiene le condivisioni disponibili per un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4cf74-103">Gets the available shares for a device.</span></span>

## <span data-ttu-id="4cf74-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4cf74-104">SYNTAX</span></span>

### <span data-ttu-id="4cf74-105">ListParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4cf74-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4cf74-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4cf74-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeShare -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4cf74-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="4cf74-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4cf74-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4cf74-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeShare [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="4cf74-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4cf74-109">DESCRIPTION</span></span>
<span data-ttu-id="4cf74-110">Il cmdlet **Get-AzDataBoxEdgeShare** ottiene le condivisioni disponibili per un dispositivo Edge della casella dati.</span><span class="sxs-lookup"><span data-stu-id="4cf74-110">The **Get-AzDataBoxEdgeShare** cmdlet gets the available shares for a Data Box Edge device.</span></span> <span data-ttu-id="4cf74-111">Se viene fornito il nome, otterrà il nome della condivisione.</span><span class="sxs-lookup"><span data-stu-id="4cf74-111">If Name is provided this will get the share by Name.</span></span>

## <span data-ttu-id="4cf74-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4cf74-112">EXAMPLES</span></span>

### <span data-ttu-id="4cf74-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4cf74-113">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-1    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-2    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-3    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-4    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
```

## <span data-ttu-id="4cf74-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4cf74-114">PARAMETERS</span></span>

### <span data-ttu-id="4cf74-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cf74-115">-DefaultProfile</span></span>
<span data-ttu-id="4cf74-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4cf74-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4cf74-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="4cf74-117">-DeviceName</span></span>
<span data-ttu-id="4cf74-118">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="4cf74-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cf74-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="4cf74-119">-DeviceObject</span></span>
<span data-ttu-id="4cf74-120">Immettere l'oggetto dispositivo corrispondente</span><span class="sxs-lookup"><span data-stu-id="4cf74-120">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4cf74-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="4cf74-121">-Name</span></span>
<span data-ttu-id="4cf74-122">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="4cf74-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cf74-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4cf74-123">-ResourceGroupName</span></span>
<span data-ttu-id="4cf74-124">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="4cf74-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cf74-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4cf74-125">-ResourceId</span></span>
<span data-ttu-id="4cf74-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="4cf74-126">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cf74-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cf74-127">CommonParameters</span></span>
<span data-ttu-id="4cf74-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4cf74-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cf74-129">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4cf74-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cf74-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4cf74-130">INPUTS</span></span>

### <span data-ttu-id="4cf74-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="4cf74-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="4cf74-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4cf74-132">OUTPUTS</span></span>

### <span data-ttu-id="4cf74-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="4cf74-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span></span>

## <span data-ttu-id="4cf74-134">Note</span><span class="sxs-lookup"><span data-stu-id="4cf74-134">NOTES</span></span>

## <span data-ttu-id="4cf74-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4cf74-135">RELATED LINKS</span></span>
