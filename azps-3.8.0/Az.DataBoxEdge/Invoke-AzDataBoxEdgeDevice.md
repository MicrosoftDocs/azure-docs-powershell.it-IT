---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/invoke-azdataboxedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeDevice.md
ms.openlocfilehash: 29bf8cf612d3569480c62784466879095ebcdb6e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94021363"
---
# <span data-ttu-id="c83cb-101">Invoke-AzDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="c83cb-101">Invoke-AzDataBoxEdgeDevice</span></span>

## <span data-ttu-id="c83cb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c83cb-102">SYNOPSIS</span></span>
<span data-ttu-id="c83cb-103">Richiama azioni specifiche nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c83cb-103">Invokes specific actions on the device.</span></span>

## <span data-ttu-id="c83cb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c83cb-104">SYNTAX</span></span>

### <span data-ttu-id="c83cb-105">InvokeScanForUpdateParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c83cb-105">InvokeScanForUpdateParameterSet (Default)</span></span>
```
Invoke-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c83cb-106">InvokeFetchUpdatesByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c83cb-106">InvokeFetchUpdatesByResourceIdParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -ResourceId <String> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c83cb-107">InvokeInstallUpdatesByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c83cb-107">InvokeInstallUpdatesByResourceIdParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -ResourceId <String> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c83cb-108">InvokeScanForUpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c83cb-108">InvokeScanForUpdateByResourceIdParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -ResourceId <String> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c83cb-109">InvokeInstallUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="c83cb-109">InvokeInstallUpdateParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c83cb-110">InvokeFetchUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="c83cb-110">InvokeFetchUpdateParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c83cb-111">InvokeFetchUpdatesByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c83cb-111">InvokeFetchUpdatesByDeviceObjectParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -DeviceObject <PSDataBoxEdgeDevice> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c83cb-112">InvokeScanForUpdateByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c83cb-112">InvokeScanForUpdateByDeviceObjectParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -DeviceObject <PSDataBoxEdgeDevice> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c83cb-113">InvokeInstallUpdatesByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c83cb-113">InvokeInstallUpdatesByDeviceObjectParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -DeviceObject <PSDataBoxEdgeDevice> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c83cb-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c83cb-114">DESCRIPTION</span></span>
<span data-ttu-id="c83cb-115">Il cmdlet **Invoke-AzDataBoxEdgeDevice** richiama le azioni per analizzare, scaricare e installare gli aggiornamenti nel dispositivo Edge della casella dati.</span><span class="sxs-lookup"><span data-stu-id="c83cb-115">The **Invoke-AzDataBoxEdgeDevice** cmdlet invokes actions to scan, download �and install the updates on the Data Box Edge device.</span></span> <span data-ttu-id="c83cb-116">Un'analisi automatica viene eseguita giornalmente sul dispositivo, è possibile attivare l'analisi in modo esplicito eseguendo questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c83cb-116">An automatic scan runs on the device daily, you can trigger the scan explicitly by running this cmdlet.</span></span>

## <span data-ttu-id="c83cb-117">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c83cb-117">EXAMPLES</span></span>

### <span data-ttu-id="c83cb-118">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c83cb-118">Example 1</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -ScanForUpdate
```

### <span data-ttu-id="c83cb-119">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="c83cb-119">Example 2</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -FetchUpdate
```

### <span data-ttu-id="c83cb-120">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="c83cb-120">Example 3</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -InstallUpdate
```

## <span data-ttu-id="c83cb-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c83cb-121">PARAMETERS</span></span>

### <span data-ttu-id="c83cb-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c83cb-122">-AsJob</span></span>
<span data-ttu-id="c83cb-123">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="c83cb-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c83cb-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c83cb-124">-DefaultProfile</span></span>
<span data-ttu-id="c83cb-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c83cb-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c83cb-126">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="c83cb-126">-DeviceObject</span></span>
<span data-ttu-id="c83cb-127">Immettere l'oggetto dispositivo corrispondente</span><span class="sxs-lookup"><span data-stu-id="c83cb-127">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="c83cb-128">-FetchUpdate</span><span class="sxs-lookup"><span data-stu-id="c83cb-128">-FetchUpdate</span></span>
<span data-ttu-id="c83cb-129">Scarica gli aggiornamenti in una casella dati Edge/Device gateway</span><span class="sxs-lookup"><span data-stu-id="c83cb-129">Downloads the updates on a data box edge/gateway device</span></span>

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

### <span data-ttu-id="c83cb-130">-InstallUpdate</span><span class="sxs-lookup"><span data-stu-id="c83cb-130">-InstallUpdate</span></span>
<span data-ttu-id="c83cb-131">Installa gli aggiornamenti nel dispositivo Edge/Gateway della casella dati</span><span class="sxs-lookup"><span data-stu-id="c83cb-131">Installs the updates on the data box edge/gateway device</span></span>

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

### <span data-ttu-id="c83cb-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="c83cb-132">-Name</span></span>
<span data-ttu-id="c83cb-133">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="c83cb-133">Device Name</span></span>

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

### <span data-ttu-id="c83cb-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c83cb-134">-PassThru</span></span>
<span data-ttu-id="c83cb-135">Restituisce vero in caso di esito positivo</span><span class="sxs-lookup"><span data-stu-id="c83cb-135">returns true if successful</span></span>

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

### <span data-ttu-id="c83cb-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c83cb-136">-ResourceGroupName</span></span>
<span data-ttu-id="c83cb-137">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="c83cb-137">Resource Group Name</span></span>

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

### <span data-ttu-id="c83cb-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c83cb-138">-ResourceId</span></span>
<span data-ttu-id="c83cb-139">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="c83cb-139">Azure ResourceId</span></span>

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

### <span data-ttu-id="c83cb-140">-ScanForUpdate</span><span class="sxs-lookup"><span data-stu-id="c83cb-140">-ScanForUpdate</span></span>
<span data-ttu-id="c83cb-141">Analizza gli aggiornamenti in un dispositivo Edge/Gateway della casella dati.</span><span class="sxs-lookup"><span data-stu-id="c83cb-141">Scans for updates on a data box edge/gateway device.</span></span>

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

### <span data-ttu-id="c83cb-142">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c83cb-142">-Confirm</span></span>
<span data-ttu-id="c83cb-143">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c83cb-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c83cb-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c83cb-144">-WhatIf</span></span>
<span data-ttu-id="c83cb-145">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c83cb-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c83cb-146">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c83cb-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c83cb-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c83cb-147">CommonParameters</span></span>
<span data-ttu-id="c83cb-148">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c83cb-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c83cb-149">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c83cb-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c83cb-150">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c83cb-150">INPUTS</span></span>

### <span data-ttu-id="c83cb-151">Nessuno</span><span class="sxs-lookup"><span data-stu-id="c83cb-151">None</span></span>

## <span data-ttu-id="c83cb-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c83cb-152">OUTPUTS</span></span>

### <span data-ttu-id="c83cb-153">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c83cb-153">System.Boolean</span></span>

## <span data-ttu-id="c83cb-154">Note</span><span class="sxs-lookup"><span data-stu-id="c83cb-154">NOTES</span></span>

## <span data-ttu-id="c83cb-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c83cb-155">RELATED LINKS</span></span>
