---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeShare.md
ms.openlocfilehash: 0e0d0e3b2dfca824d66a9a75f3e22438335c97db
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019017"
---
# <span data-ttu-id="5ae74-101">Get-AzStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="5ae74-101">Get-AzStackEdgeShare</span></span>

## <span data-ttu-id="5ae74-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5ae74-102">SYNOPSIS</span></span>
<span data-ttu-id="5ae74-103">Ottiene le condivisioni disponibili per un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5ae74-103">Gets the available shares for a device.</span></span>

## <span data-ttu-id="5ae74-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5ae74-104">SYNTAX</span></span>

### <span data-ttu-id="5ae74-105">ListParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5ae74-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ae74-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5ae74-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeShare -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ae74-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="5ae74-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ae74-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5ae74-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeShare [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="5ae74-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5ae74-109">DESCRIPTION</span></span>
<span data-ttu-id="5ae74-110">Il cmdlet **Get-AzStackEdgeShare** ottiene le condivisioni disponibili per un dispositivo Edge dello stack.</span><span class="sxs-lookup"><span data-stu-id="5ae74-110">The **Get-AzStackEdgeShare** cmdlet gets the available shares for a Stack Edge device.</span></span> <span data-ttu-id="5ae74-111">Se viene fornito il nome, otterrà il nome della condivisione.</span><span class="sxs-lookup"><span data-stu-id="5ae74-111">If Name is provided this will get the share by Name.</span></span>

## <span data-ttu-id="5ae74-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5ae74-112">EXAMPLES</span></span>

### <span data-ttu-id="5ae74-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5ae74-113">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-1    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-2    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-3    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-4    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
```

## <span data-ttu-id="5ae74-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5ae74-114">PARAMETERS</span></span>

### <span data-ttu-id="5ae74-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ae74-115">-DefaultProfile</span></span>
<span data-ttu-id="5ae74-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5ae74-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ae74-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="5ae74-117">-DeviceName</span></span>
<span data-ttu-id="5ae74-118">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="5ae74-118">Device Name</span></span>

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

### <span data-ttu-id="5ae74-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="5ae74-119">-DeviceObject</span></span>
<span data-ttu-id="5ae74-120">Immettere l'oggetto dispositivo corrispondente</span><span class="sxs-lookup"><span data-stu-id="5ae74-120">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice
Parameter Sets: GetByParentObjectParameterSet
Aliases: Device

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5ae74-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="5ae74-121">-Name</span></span>
<span data-ttu-id="5ae74-122">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="5ae74-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: EdgeShareName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: EdgeShareName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ae74-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ae74-123">-ResourceGroupName</span></span>
<span data-ttu-id="5ae74-124">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="5ae74-124">Resource Group Name</span></span>

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

### <span data-ttu-id="5ae74-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5ae74-125">-ResourceId</span></span>
<span data-ttu-id="5ae74-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="5ae74-126">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ae74-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ae74-127">CommonParameters</span></span>
<span data-ttu-id="5ae74-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ae74-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ae74-129">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5ae74-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ae74-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5ae74-130">INPUTS</span></span>

### <span data-ttu-id="5ae74-131">Microsoft. Azure. PowerShell. Cmdlets. StackEdge. Models. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="5ae74-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="5ae74-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5ae74-132">OUTPUTS</span></span>

### <span data-ttu-id="5ae74-133">Microsoft. Azure. PowerShell. Cmdlets. StackEdge. Models. PSStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="5ae74-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span></span>

## <span data-ttu-id="5ae74-134">Note</span><span class="sxs-lookup"><span data-stu-id="5ae74-134">NOTES</span></span>

## <span data-ttu-id="5ae74-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5ae74-135">RELATED LINKS</span></span>
