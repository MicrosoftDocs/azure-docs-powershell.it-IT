---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/invoke-azdataboxedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeDevice.md
ms.openlocfilehash: 29bf8cf612d3569480c62784466879095ebcdb6e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194895"
---
# <span data-ttu-id="39a8f-101">Invoke-AzDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="39a8f-101">Invoke-AzDataBoxEdgeDevice</span></span>

## <span data-ttu-id="39a8f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39a8f-102">SYNOPSIS</span></span>
<span data-ttu-id="39a8f-103">Richiama azioni specifiche nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="39a8f-103">Invokes specific actions on the device.</span></span>

## <span data-ttu-id="39a8f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="39a8f-104">SYNTAX</span></span>

### <span data-ttu-id="39a8f-105">InvokeScanForUpdateParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="39a8f-105">InvokeScanForUpdateParameterSet (Default)</span></span>
```
Invoke-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39a8f-106">InvokeFetchUpdatesByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="39a8f-106">InvokeFetchUpdatesByResourceIdParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -ResourceId <String> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39a8f-107">InvokeInstallUpdatesByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="39a8f-107">InvokeInstallUpdatesByResourceIdParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -ResourceId <String> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39a8f-108">InvokeScanForUpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="39a8f-108">InvokeScanForUpdateByResourceIdParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -ResourceId <String> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39a8f-109">InvokeInstallUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="39a8f-109">InvokeInstallUpdateParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39a8f-110">InvokeFetchUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="39a8f-110">InvokeFetchUpdateParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39a8f-111">InvokeFetchUpdatesByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="39a8f-111">InvokeFetchUpdatesByDeviceObjectParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -DeviceObject <PSDataBoxEdgeDevice> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39a8f-112">InvokeScanForUpdateByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="39a8f-112">InvokeScanForUpdateByDeviceObjectParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -DeviceObject <PSDataBoxEdgeDevice> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39a8f-113">InvokeInstallUpdatesByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="39a8f-113">InvokeInstallUpdatesByDeviceObjectParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -DeviceObject <PSDataBoxEdgeDevice> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39a8f-114">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="39a8f-114">DESCRIPTION</span></span>
<span data-ttu-id="39a8f-115">Il cmdlet **Invoke-AzDataBoxEdgeDevice** richiama le azioni per analizzare, scaricare e installare gli aggiornamenti nel dispositivo Data Box Edge.</span><span class="sxs-lookup"><span data-stu-id="39a8f-115">The **Invoke-AzDataBoxEdgeDevice** cmdlet invokes actions to scan, download �and install the updates on the Data Box Edge device.</span></span> <span data-ttu-id="39a8f-116">Un'analisi automatica viene eseguita quotidianamente sul dispositivo, è possibile attivarlo esplicitamente eseguendo questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39a8f-116">An automatic scan runs on the device daily, you can trigger the scan explicitly by running this cmdlet.</span></span>

## <span data-ttu-id="39a8f-117">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="39a8f-117">EXAMPLES</span></span>

### <span data-ttu-id="39a8f-118">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="39a8f-118">Example 1</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -ScanForUpdate
```

### <span data-ttu-id="39a8f-119">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="39a8f-119">Example 2</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -FetchUpdate
```

### <span data-ttu-id="39a8f-120">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="39a8f-120">Example 3</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -InstallUpdate
```

## <span data-ttu-id="39a8f-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="39a8f-121">PARAMETERS</span></span>

### <span data-ttu-id="39a8f-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="39a8f-122">-AsJob</span></span>
<span data-ttu-id="39a8f-123">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="39a8f-123">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39a8f-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39a8f-124">-DefaultProfile</span></span>
<span data-ttu-id="39a8f-125">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="39a8f-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39a8f-126">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="39a8f-126">-DeviceObject</span></span>
<span data-ttu-id="39a8f-127">Specifica l'oggetto dispositivo corrispondente</span><span class="sxs-lookup"><span data-stu-id="39a8f-127">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice
Parameter Sets: InvokeFetchUpdatesByDeviceObjectParameterSet, InvokeScanForUpdateByDeviceObjectParameterSet, InvokeInstallUpdatesByDeviceObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39a8f-128">-FetchUpdate</span><span class="sxs-lookup"><span data-stu-id="39a8f-128">-FetchUpdate</span></span>
<span data-ttu-id="39a8f-129">Scarica gli aggiornamenti in un dispositivo gateway/edge casella di dati</span><span class="sxs-lookup"><span data-stu-id="39a8f-129">Downloads the updates on a data box edge/gateway device</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: InvokeFetchUpdatesByResourceIdParameterSet, InvokeFetchUpdateParameterSet, InvokeFetchUpdatesByDeviceObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39a8f-130">-InstallUpdate</span><span class="sxs-lookup"><span data-stu-id="39a8f-130">-InstallUpdate</span></span>
<span data-ttu-id="39a8f-131">Installa gli aggiornamenti nel dispositivo gateway/edge della casella di dati</span><span class="sxs-lookup"><span data-stu-id="39a8f-131">Installs the updates on the data box edge/gateway device</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: InvokeInstallUpdatesByResourceIdParameterSet, InvokeInstallUpdateParameterSet, InvokeInstallUpdatesByDeviceObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39a8f-132">-Name</span><span class="sxs-lookup"><span data-stu-id="39a8f-132">-Name</span></span>
<span data-ttu-id="39a8f-133">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="39a8f-133">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeScanForUpdateParameterSet, InvokeInstallUpdateParameterSet, InvokeFetchUpdateParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39a8f-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="39a8f-134">-PassThru</span></span>
<span data-ttu-id="39a8f-135">restituisce true se ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="39a8f-135">returns true if successful</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39a8f-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39a8f-136">-ResourceGroupName</span></span>
<span data-ttu-id="39a8f-137">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="39a8f-137">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeScanForUpdateParameterSet, InvokeInstallUpdateParameterSet, InvokeFetchUpdateParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39a8f-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="39a8f-138">-ResourceId</span></span>
<span data-ttu-id="39a8f-139">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="39a8f-139">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeFetchUpdatesByResourceIdParameterSet, InvokeInstallUpdatesByResourceIdParameterSet, InvokeScanForUpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39a8f-140">-ScanForUpdate</span><span class="sxs-lookup"><span data-stu-id="39a8f-140">-ScanForUpdate</span></span>
<span data-ttu-id="39a8f-141">Analizza la ricerca di aggiornamenti in un dispositivo gateway/edge della casella di dati.</span><span class="sxs-lookup"><span data-stu-id="39a8f-141">Scans for updates on a data box edge/gateway device.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: InvokeScanForUpdateParameterSet, InvokeScanForUpdateByResourceIdParameterSet, InvokeScanForUpdateByDeviceObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39a8f-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="39a8f-142">-Confirm</span></span>
<span data-ttu-id="39a8f-143">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39a8f-143">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39a8f-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39a8f-144">-WhatIf</span></span>
<span data-ttu-id="39a8f-145">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="39a8f-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="39a8f-146">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="39a8f-146">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39a8f-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39a8f-147">CommonParameters</span></span>
<span data-ttu-id="39a8f-148">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39a8f-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39a8f-149">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="39a8f-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39a8f-150">INPUT</span><span class="sxs-lookup"><span data-stu-id="39a8f-150">INPUTS</span></span>

### <span data-ttu-id="39a8f-151">Nessuno</span><span class="sxs-lookup"><span data-stu-id="39a8f-151">None</span></span>

## <span data-ttu-id="39a8f-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="39a8f-152">OUTPUTS</span></span>

### <span data-ttu-id="39a8f-153">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="39a8f-153">System.Boolean</span></span>

## <span data-ttu-id="39a8f-154">NOTE</span><span class="sxs-lookup"><span data-stu-id="39a8f-154">NOTES</span></span>

## <span data-ttu-id="39a8f-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="39a8f-155">RELATED LINKS</span></span>
