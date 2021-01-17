---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesPool.md
ms.openlocfilehash: 8f26023224e0f6d4a035f4671db7b45be57a3177
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98335287"
---
# <span data-ttu-id="31b0a-101">Update-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="31b0a-101">Update-AzNetAppFilesPool</span></span>

## <span data-ttu-id="31b0a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="31b0a-102">SYNOPSIS</span></span>
<span data-ttu-id="31b0a-103">Aggiorna uno Azure NetApp file (ANF) pool in base ai modificatori facoltativi forniti.</span><span class="sxs-lookup"><span data-stu-id="31b0a-103">Updates an Azure NetApp Files (ANF) pool according to the optional modifiers provided.</span></span>

## <span data-ttu-id="31b0a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="31b0a-104">SYNTAX</span></span>

### <span data-ttu-id="31b0a-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="31b0a-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesPool -ResourceGroupName <String> [-Location <String>] -AccountName <String> -Name <String>
 [-PoolSize <Int64>] [-QosType <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31b0a-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="31b0a-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesPool -Name <String> [-PoolSize <Int64>] [-QosType <String>] [-Tag <Hashtable>]
 -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="31b0a-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="31b0a-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesPool [-PoolSize <Int64>] [-QosType <String>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31b0a-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="31b0a-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesPool [-PoolSize <Int64>] [-QosType <String>] [-Tag <Hashtable>]
 -InputObject <PSNetAppFilesPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="31b0a-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="31b0a-109">DESCRIPTION</span></span>
<span data-ttu-id="31b0a-110">Il cmdlet **Update-AzNetAppFilesPool** modifica un pool di ANF.</span><span class="sxs-lookup"><span data-stu-id="31b0a-110">The **Update-AzNetAppFilesPool** cmdlet modifies an ANF pool.</span></span>

## <span data-ttu-id="31b0a-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="31b0a-111">EXAMPLES</span></span>

### <span data-ttu-id="31b0a-112">Esempio 1: modificare un pool di ANF</span><span class="sxs-lookup"><span data-stu-id="31b0a-112">Example 1: Modify an ANF pool</span></span>
```
PS C:\>Update-AzNetAppFilesPool -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -PoolSize 4398046511104 -QosType "Auto"

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool
Name              : MyAnfAccount/MyAnfPool
Type              : Microsoft.NetApp/netAppAccounts/capacityPools
Tags              :
PoolId            : 9fa2ca6d-1e48-4439-30e3-7de056e44e5a
Size              : 4398046511104
ServiceLevel      : Standard
QosType           : Auto
ProvisioningState : Succeeded
```

<span data-ttu-id="31b0a-113">Questo comando modifica il pool di ANF "MyAnfPool" per avere le dimensioni e il QosType specificati.</span><span class="sxs-lookup"><span data-stu-id="31b0a-113">This command changes the ANF pool "MyAnfPool" to have the given size and QosType.</span></span>

## <span data-ttu-id="31b0a-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="31b0a-114">PARAMETERS</span></span>

### <span data-ttu-id="31b0a-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="31b0a-115">-AccountName</span></span>
<span data-ttu-id="31b0a-116">Nome dell'account di ANF</span><span class="sxs-lookup"><span data-stu-id="31b0a-116">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31b0a-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="31b0a-117">-AccountObject</span></span>
<span data-ttu-id="31b0a-118">L'oggetto account che contiene il pool da aggiornare</span><span class="sxs-lookup"><span data-stu-id="31b0a-118">The account object containing the pool to update</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="31b0a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31b0a-119">-DefaultProfile</span></span>
<span data-ttu-id="31b0a-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="31b0a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31b0a-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="31b0a-121">-InputObject</span></span>
<span data-ttu-id="31b0a-122">Oggetto pool da aggiornare</span><span class="sxs-lookup"><span data-stu-id="31b0a-122">The pool object to update</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="31b0a-123">-Posizione</span><span class="sxs-lookup"><span data-stu-id="31b0a-123">-Location</span></span>
<span data-ttu-id="31b0a-124">Posizione della risorsa</span><span class="sxs-lookup"><span data-stu-id="31b0a-124">The location of the resource</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31b0a-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="31b0a-125">-Name</span></span>
<span data-ttu-id="31b0a-126">Nome del pool di ANF</span><span class="sxs-lookup"><span data-stu-id="31b0a-126">The name of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: PoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31b0a-127">-PoolSize</span><span class="sxs-lookup"><span data-stu-id="31b0a-127">-PoolSize</span></span>
<span data-ttu-id="31b0a-128">Dimensioni del pool di ANF</span><span class="sxs-lookup"><span data-stu-id="31b0a-128">The size of the ANF pool</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31b0a-129">-QosType</span><span class="sxs-lookup"><span data-stu-id="31b0a-129">-QosType</span></span>
<span data-ttu-id="31b0a-130">Tipo QoS del pool.</span><span class="sxs-lookup"><span data-stu-id="31b0a-130">The qos type of the pool.</span></span> <span data-ttu-id="31b0a-131">I valori possibili includono:' auto ',' manual '</span><span class="sxs-lookup"><span data-stu-id="31b0a-131">Possible values include: 'Auto', 'Manual'</span></span>

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

### <span data-ttu-id="31b0a-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31b0a-132">-ResourceGroupName</span></span>
<span data-ttu-id="31b0a-133">Gruppo risorse dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="31b0a-133">The resource group of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31b0a-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="31b0a-134">-ResourceId</span></span>
<span data-ttu-id="31b0a-135">ID risorsa del pool di ANF</span><span class="sxs-lookup"><span data-stu-id="31b0a-135">The resource id of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31b0a-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="31b0a-136">-Tag</span></span>
<span data-ttu-id="31b0a-137">Hashtable che rappresenta i tag delle risorse</span><span class="sxs-lookup"><span data-stu-id="31b0a-137">A hashtable which represents resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31b0a-138">-Confermare</span><span class="sxs-lookup"><span data-stu-id="31b0a-138">-Confirm</span></span>
<span data-ttu-id="31b0a-139">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="31b0a-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31b0a-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31b0a-140">-WhatIf</span></span>
<span data-ttu-id="31b0a-141">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="31b0a-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31b0a-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="31b0a-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31b0a-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31b0a-143">CommonParameters</span></span>
<span data-ttu-id="31b0a-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31b0a-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31b0a-145">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="31b0a-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31b0a-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="31b0a-146">INPUTS</span></span>

### <span data-ttu-id="31b0a-147">System. String</span><span class="sxs-lookup"><span data-stu-id="31b0a-147">System.String</span></span>

### <span data-ttu-id="31b0a-148">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="31b0a-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="31b0a-149">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="31b0a-149">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="31b0a-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="31b0a-150">OUTPUTS</span></span>

### <span data-ttu-id="31b0a-151">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="31b0a-151">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="31b0a-152">Note</span><span class="sxs-lookup"><span data-stu-id="31b0a-152">NOTES</span></span>

## <span data-ttu-id="31b0a-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="31b0a-153">RELATED LINKS</span></span>
