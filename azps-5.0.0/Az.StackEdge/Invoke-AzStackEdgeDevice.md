---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/invoke-azstackedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Invoke-AzStackEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Invoke-AzStackEdgeDevice.md
ms.openlocfilehash: f25aeb501ff046a25330ad5db47bbdb06fbe7b35
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302388"
---
# <span data-ttu-id="e2122-101">Invoke-AzStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="e2122-101">Invoke-AzStackEdgeDevice</span></span>

## <span data-ttu-id="e2122-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e2122-102">SYNOPSIS</span></span>
<span data-ttu-id="e2122-103">Richiama azioni specifiche nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e2122-103">Invokes specific actions on the device.</span></span>

## <span data-ttu-id="e2122-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e2122-104">SYNTAX</span></span>

### <span data-ttu-id="e2122-105">InvokeScanForUpdateParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e2122-105">InvokeScanForUpdateParameterSet (Default)</span></span>
```
Invoke-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2122-106">InvokeFetchUpdatesByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2122-106">InvokeFetchUpdatesByResourceIdParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -ResourceId <String> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2122-107">InvokeInstallUpdatesByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2122-107">InvokeInstallUpdatesByResourceIdParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -ResourceId <String> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2122-108">InvokeScanForUpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2122-108">InvokeScanForUpdateByResourceIdParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -ResourceId <String> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2122-109">InvokeInstallUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2122-109">InvokeInstallUpdateParameterSet</span></span>
```
Invoke-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2122-110">InvokeFetchUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2122-110">InvokeFetchUpdateParameterSet</span></span>
```
Invoke-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2122-111">InvokeFetchUpdatesByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2122-111">InvokeFetchUpdatesByDeviceObjectParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -DeviceObject <PSStackEdgeDevice> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2122-112">InvokeScanForUpdateByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2122-112">InvokeScanForUpdateByDeviceObjectParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -DeviceObject <PSStackEdgeDevice> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2122-113">InvokeInstallUpdatesByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2122-113">InvokeInstallUpdatesByDeviceObjectParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -DeviceObject <PSStackEdgeDevice> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2122-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e2122-114">DESCRIPTION</span></span>
<span data-ttu-id="e2122-115">Il cmdlet **Invoke-AzStackEdgeDevice** richiama le azioni per analizzare, scaricare e installare gli aggiornamenti nel dispositivo stack Edge.</span><span class="sxs-lookup"><span data-stu-id="e2122-115">The **Invoke-AzStackEdgeDevice** cmdlet invokes actions to scan, download �and install the updates on the Stack Edge device.</span></span> <span data-ttu-id="e2122-116">Un'analisi automatica viene eseguita giornalmente sul dispositivo, è possibile attivare l'analisi in modo esplicito eseguendo questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2122-116">An automatic scan runs on the device daily, you can trigger the scan explicitly by running this cmdlet.</span></span>

## <span data-ttu-id="e2122-117">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e2122-117">EXAMPLES</span></span>

### <span data-ttu-id="e2122-118">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e2122-118">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -ScanForUpdate
```

### <span data-ttu-id="e2122-119">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="e2122-119">Example 2</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -FetchUpdate
```

### <span data-ttu-id="e2122-120">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="e2122-120">Example 3</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -InstallUpdate
```

## <span data-ttu-id="e2122-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e2122-121">PARAMETERS</span></span>

### <span data-ttu-id="e2122-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e2122-122">-AsJob</span></span>
<span data-ttu-id="e2122-123">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="e2122-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e2122-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2122-124">-DefaultProfile</span></span>
<span data-ttu-id="e2122-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e2122-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2122-126">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="e2122-126">-DeviceObject</span></span>
<span data-ttu-id="e2122-127">Immettere l'oggetto dispositivo corrispondente</span><span class="sxs-lookup"><span data-stu-id="e2122-127">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice
Parameter Sets: InvokeFetchUpdatesByDeviceObjectParameterSet, InvokeScanForUpdateByDeviceObjectParameterSet, InvokeInstallUpdatesByDeviceObjectParameterSet
Aliases: Device

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2122-128">-FetchUpdate</span><span class="sxs-lookup"><span data-stu-id="e2122-128">-FetchUpdate</span></span>
<span data-ttu-id="e2122-129">Scarica gli aggiornamenti in uno stack Edge/dispositivo gateway</span><span class="sxs-lookup"><span data-stu-id="e2122-129">Downloads the updates on a Stack edge/gateway device</span></span>

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

### <span data-ttu-id="e2122-130">-InstallUpdate</span><span class="sxs-lookup"><span data-stu-id="e2122-130">-InstallUpdate</span></span>
<span data-ttu-id="e2122-131">Installa gli aggiornamenti nel dispositivo gateway/Edge della pila</span><span class="sxs-lookup"><span data-stu-id="e2122-131">Installs the updates on the Stack edge/gateway device</span></span>

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

### <span data-ttu-id="e2122-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="e2122-132">-Name</span></span>
<span data-ttu-id="e2122-133">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="e2122-133">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeScanForUpdateParameterSet, InvokeInstallUpdateParameterSet, InvokeFetchUpdateParameterSet
Aliases: DeviceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2122-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e2122-134">-PassThru</span></span>
<span data-ttu-id="e2122-135">Restituisce vero in caso di esito positivo</span><span class="sxs-lookup"><span data-stu-id="e2122-135">returns true if successful</span></span>

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

### <span data-ttu-id="e2122-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2122-136">-ResourceGroupName</span></span>
<span data-ttu-id="e2122-137">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="e2122-137">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeScanForUpdateParameterSet, InvokeInstallUpdateParameterSet, InvokeFetchUpdateParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2122-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e2122-138">-ResourceId</span></span>
<span data-ttu-id="e2122-139">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="e2122-139">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeFetchUpdatesByResourceIdParameterSet, InvokeInstallUpdatesByResourceIdParameterSet, InvokeScanForUpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2122-140">-ScanForUpdate</span><span class="sxs-lookup"><span data-stu-id="e2122-140">-ScanForUpdate</span></span>
<span data-ttu-id="e2122-141">Analizza gli aggiornamenti in uno stack Edge/dispositivo gateway.</span><span class="sxs-lookup"><span data-stu-id="e2122-141">Scans for updates on a Stack edge/gateway device.</span></span>

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

### <span data-ttu-id="e2122-142">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e2122-142">-Confirm</span></span>
<span data-ttu-id="e2122-143">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2122-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2122-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2122-144">-WhatIf</span></span>
<span data-ttu-id="e2122-145">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e2122-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e2122-146">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e2122-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2122-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2122-147">CommonParameters</span></span>
<span data-ttu-id="e2122-148">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2122-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2122-149">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e2122-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2122-150">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e2122-150">INPUTS</span></span>

### <span data-ttu-id="e2122-151">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e2122-151">None</span></span>

## <span data-ttu-id="e2122-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e2122-152">OUTPUTS</span></span>

### <span data-ttu-id="e2122-153">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e2122-153">System.Boolean</span></span>

## <span data-ttu-id="e2122-154">Note</span><span class="sxs-lookup"><span data-stu-id="e2122-154">NOTES</span></span>

## <span data-ttu-id="e2122-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e2122-155">RELATED LINKS</span></span>
