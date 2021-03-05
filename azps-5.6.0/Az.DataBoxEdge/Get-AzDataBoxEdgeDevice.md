---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/get-azdataboxedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeDevice.md
ms.openlocfilehash: f02cda5fe04ed72a5e6defd382c372b40c9c039b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998099"
---
# <span data-ttu-id="c2a93-101">Get-AzDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="c2a93-101">Get-AzDataBoxEdgeDevice</span></span>

## <span data-ttu-id="c2a93-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2a93-102">SYNOPSIS</span></span>
<span data-ttu-id="c2a93-103">Recupera le informazioni sui dispositivi Microsoft Data Box Edge disponibili.</span><span class="sxs-lookup"><span data-stu-id="c2a93-103">Gets the information on available Data Box Edge devices.</span></span>

## <span data-ttu-id="c2a93-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c2a93-104">SYNTAX</span></span>

### <span data-ttu-id="c2a93-105">ListByParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c2a93-105">ListByParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeDevice [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c2a93-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2a93-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2a93-107">GetExtendedInfoByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2a93-107">GetExtendedInfoByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice -ResourceId <String> [-ExtendedInfo] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c2a93-108">GetNetworkSettingByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2a93-108">GetNetworkSettingByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice -ResourceId <String> [-NetworkSetting] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c2a93-109">GetSummaryUpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2a93-109">GetSummaryUpdateByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice -ResourceId <String> [-UpdateSummary] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c2a93-110">GetAlertByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2a93-110">GetAlertByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice -ResourceId <String> [-Alert] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c2a93-111">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2a93-111">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2a93-112">GetSummaryUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2a93-112">GetSummaryUpdateParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-UpdateSummary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2a93-113">GetNetworkSettingParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2a93-113">GetNetworkSettingParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-NetworkSetting]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2a93-114">GetExtendedInfoParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2a93-114">GetExtendedInfoParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-ExtendedInfo]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2a93-115">GetAlertParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2a93-115">GetAlertParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-Alert]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2a93-116">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c2a93-116">DESCRIPTION</span></span>
<span data-ttu-id="c2a93-117">Il cmdlet **Get-AzDataBoxEdgeDevice** ottiene le informazioni sui dispositivi perimetrali della casella di dati disponibili.</span><span class="sxs-lookup"><span data-stu-id="c2a93-117">The **Get-AzDataBoxEdgeDevice** cmdlet gets the information about the available Data Box Edge Devices.</span></span> <span data-ttu-id="c2a93-118">È possibile specificare il nome del dispositivo insieme al nome del gruppo di risorse per ottenere le informazioni in un dispositivo specifico.</span><span class="sxs-lookup"><span data-stu-id="c2a93-118">You can specify the Name of the device along with the Resource Group Name to get the information on a specific device.</span></span> 

## <span data-ttu-id="c2a93-119">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c2a93-119">EXAMPLES</span></span>

### <span data-ttu-id="c2a93-120">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c2a93-120">Example 1</span></span>
```powershell
PS C:\>Get-AzDataBoxEdgeDevice
Name               ResourceGroupName  Model   Location
----               -----------------  -----   --------
deviceNameOne      resourceGroupName1 Edge    eastus
deviceNameTwo      resourceGroupName2 Edge    westus
deviceNameThree    resourceGroupName3 Gateway eastus
```

### <span data-ttu-id="c2a93-121">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="c2a93-121">Example 2</span></span>
```powershell
PS C:\>Get-AzDataBoxEdgeDevice -ResourceId /subscriptions/subscriptionId/resourcegroups/resourceGroupName/providers/Microsoft.DataBoxEdge/dataBoxEdgeDevices/deviceName
Name            ResourceGroupName    Model   Location
----            -----------------    -----   --------
deviceName      resourceGroupName    Edge    eastus
```

### <span data-ttu-id="c2a93-122">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="c2a93-122">Example 3</span></span>
```powershell
PS C:\>Get-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -DeviceName deviceName
Name            ResourceGroupName    Model   Location
----            -----------------    -----   --------
deviceName      resourceGroupName    Edge    eastus
```

## <span data-ttu-id="c2a93-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c2a93-123">PARAMETERS</span></span>

### <span data-ttu-id="c2a93-124">-Avviso</span><span class="sxs-lookup"><span data-stu-id="c2a93-124">-Alert</span></span>
<span data-ttu-id="c2a93-125">Recuperare gli avvisi nel dispositivo gateway/edge della casella dei dati</span><span class="sxs-lookup"><span data-stu-id="c2a93-125">Fetch the alerts on the data box edge/gateway device</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetAlertByResourceIdParameterSet, GetAlertParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2a93-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2a93-126">-DefaultProfile</span></span>
<span data-ttu-id="c2a93-127">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c2a93-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2a93-128">-ExtendedInfo</span><span class="sxs-lookup"><span data-stu-id="c2a93-128">-ExtendedInfo</span></span>
<span data-ttu-id="c2a93-129">Recupera informazioni aggiuntive per il dispositivo gateway della casella di dati o del gateway della casella di dati specificato</span><span class="sxs-lookup"><span data-stu-id="c2a93-129">Gets additional information for the specified Data Box Edge/Data Box Gateway device</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetExtendedInfoByResourceIdParameterSet, GetExtendedInfoParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2a93-130">-Name</span><span class="sxs-lookup"><span data-stu-id="c2a93-130">-Name</span></span>
<span data-ttu-id="c2a93-131">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="c2a93-131">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetSummaryUpdateParameterSet, GetNetworkSettingParameterSet, GetExtendedInfoParameterSet, GetAlertParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2a93-132">-NetworkSetting</span><span class="sxs-lookup"><span data-stu-id="c2a93-132">-NetworkSetting</span></span>
<span data-ttu-id="c2a93-133">Recupera le impostazioni di rete del dispositivo gateway della casella di dati/Edge della casella di dati specificato</span><span class="sxs-lookup"><span data-stu-id="c2a93-133">Gets the network settings of the specified Data Box Edge/Data Box Gateway device</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetNetworkSettingByResourceIdParameterSet, GetNetworkSettingParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2a93-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2a93-134">-ResourceGroupName</span></span>
<span data-ttu-id="c2a93-135">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="c2a93-135">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListByParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetSummaryUpdateParameterSet, GetNetworkSettingParameterSet, GetExtendedInfoParameterSet, GetAlertParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2a93-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c2a93-136">-ResourceId</span></span>
<span data-ttu-id="c2a93-137">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="c2a93-137">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet, GetExtendedInfoByResourceIdParameterSet, GetNetworkSettingByResourceIdParameterSet, GetSummaryUpdateByResourceIdParameterSet, GetAlertByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2a93-138">-UpdateSummary</span><span class="sxs-lookup"><span data-stu-id="c2a93-138">-UpdateSummary</span></span>
<span data-ttu-id="c2a93-139">Ottiene informazioni sulla disponibilità degli aggiornamenti in base all'ultima analisi del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c2a93-139">Gets information about the availability of updates based on the last scan of the device.</span></span> <span data-ttu-id="c2a93-140">Riceve anche informazioni sui processi di download o installazione in corso nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c2a93-140">It also gets information about any ongoing download or install jobs on the device.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetSummaryUpdateByResourceIdParameterSet, GetSummaryUpdateParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2a93-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2a93-141">CommonParameters</span></span>
<span data-ttu-id="c2a93-142">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2a93-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2a93-143">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c2a93-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2a93-144">INPUT</span><span class="sxs-lookup"><span data-stu-id="c2a93-144">INPUTS</span></span>

### <span data-ttu-id="c2a93-145">Nessuno</span><span class="sxs-lookup"><span data-stu-id="c2a93-145">None</span></span>

## <span data-ttu-id="c2a93-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c2a93-146">OUTPUTS</span></span>

### <span data-ttu-id="c2a93-147">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="c2a93-147">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

### <span data-ttu-id="c2a93-148">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeNetwork Collega</span><span class="sxs-lookup"><span data-stu-id="c2a93-148">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeNetworkAdapter</span></span>

### <span data-ttu-id="c2a93-149">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDeviceExtendedInfo</span><span class="sxs-lookup"><span data-stu-id="c2a93-149">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDeviceExtendedInfo</span></span>

### <span data-ttu-id="c2a93-150">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUpdateSummary</span><span class="sxs-lookup"><span data-stu-id="c2a93-150">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUpdateSummary</span></span>

### <span data-ttu-id="c2a93-151">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeAlert</span><span class="sxs-lookup"><span data-stu-id="c2a93-151">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeAlert</span></span>

## <span data-ttu-id="c2a93-152">NOTE</span><span class="sxs-lookup"><span data-stu-id="c2a93-152">NOTES</span></span>

## <span data-ttu-id="c2a93-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c2a93-153">RELATED LINKS</span></span>
