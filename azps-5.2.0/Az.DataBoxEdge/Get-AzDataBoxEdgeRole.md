---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeRole.md
ms.openlocfilehash: 9bda923d7a0e7e999ae8368fd648ee6745cbb226
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98362809"
---
# <span data-ttu-id="267cf-101">Get-AzDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="267cf-101">Get-AzDataBoxEdgeRole</span></span>

## <span data-ttu-id="267cf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="267cf-102">SYNOPSIS</span></span>
<span data-ttu-id="267cf-103">Recupera i ruoli disponibili per un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="267cf-103">Fetches the available roles for a device.</span></span>

## <span data-ttu-id="267cf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="267cf-104">SYNTAX</span></span>

### <span data-ttu-id="267cf-105">ListParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="267cf-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="267cf-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="267cf-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeRole -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="267cf-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="267cf-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="267cf-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="267cf-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeRole [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="267cf-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="267cf-109">DESCRIPTION</span></span>
<span data-ttu-id="267cf-110">Il cmdlet **Get-AzDataBoxEdgeRole** recupera i ruoli disponibili per un dispositivo Edge della casella dati.</span><span class="sxs-lookup"><span data-stu-id="267cf-110">The **Get-AzDataBoxEdgeRole** cmdlet fetches the available IoT roles for a Data Box Edge device.</span></span> <span data-ttu-id="267cf-111">Puoi menzionare il parametro Name per ottenere i dettagli di un ruolo specifico.</span><span class="sxs-lookup"><span data-stu-id="267cf-111">You can mention the Name parameter to get the details of a specific IoT role.</span></span>

## <span data-ttu-id="267cf-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="267cf-112">EXAMPLES</span></span>

### <span data-ttu-id="267cf-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="267cf-113">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
iotrole ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

## <span data-ttu-id="267cf-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="267cf-114">PARAMETERS</span></span>

### <span data-ttu-id="267cf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="267cf-115">-DefaultProfile</span></span>
<span data-ttu-id="267cf-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="267cf-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="267cf-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="267cf-117">-DeviceName</span></span>
<span data-ttu-id="267cf-118">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="267cf-118">Device Name</span></span>

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

### <span data-ttu-id="267cf-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="267cf-119">-DeviceObject</span></span>
<span data-ttu-id="267cf-120">Immettere l'oggetto dispositivo corrispondente</span><span class="sxs-lookup"><span data-stu-id="267cf-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="267cf-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="267cf-121">-Name</span></span>
<span data-ttu-id="267cf-122">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="267cf-122">Resource Name</span></span>

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

### <span data-ttu-id="267cf-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="267cf-123">-ResourceGroupName</span></span>
<span data-ttu-id="267cf-124">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="267cf-124">Resource Group Name</span></span>

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

### <span data-ttu-id="267cf-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="267cf-125">-ResourceId</span></span>
<span data-ttu-id="267cf-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="267cf-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="267cf-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="267cf-127">CommonParameters</span></span>
<span data-ttu-id="267cf-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="267cf-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="267cf-129">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="267cf-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="267cf-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="267cf-130">INPUTS</span></span>

### <span data-ttu-id="267cf-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="267cf-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="267cf-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="267cf-132">OUTPUTS</span></span>

### <span data-ttu-id="267cf-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="267cf-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span></span>

## <span data-ttu-id="267cf-134">Note</span><span class="sxs-lookup"><span data-stu-id="267cf-134">NOTES</span></span>

## <span data-ttu-id="267cf-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="267cf-135">RELATED LINKS</span></span>
