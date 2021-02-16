---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesPool.md
ms.openlocfilehash: 8f26023224e0f6d4a035f4671db7b45be57a3177
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179958"
---
# <span data-ttu-id="42546-101">Update-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="42546-101">Update-AzNetAppFilesPool</span></span>

## <span data-ttu-id="42546-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42546-102">SYNOPSIS</span></span>
<span data-ttu-id="42546-103">Aggiorna un pool di file ANF (Azure NetApp Files) in base ai modificatori facoltativi disponibili.</span><span class="sxs-lookup"><span data-stu-id="42546-103">Updates an Azure NetApp Files (ANF) pool according to the optional modifiers provided.</span></span>

## <span data-ttu-id="42546-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="42546-104">SYNTAX</span></span>

### <span data-ttu-id="42546-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="42546-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesPool -ResourceGroupName <String> [-Location <String>] -AccountName <String> -Name <String>
 [-PoolSize <Int64>] [-QosType <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42546-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="42546-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesPool -Name <String> [-PoolSize <Int64>] [-QosType <String>] [-Tag <Hashtable>]
 -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="42546-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="42546-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesPool [-PoolSize <Int64>] [-QosType <String>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42546-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="42546-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesPool [-PoolSize <Int64>] [-QosType <String>] [-Tag <Hashtable>]
 -InputObject <PSNetAppFilesPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="42546-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="42546-109">DESCRIPTION</span></span>
<span data-ttu-id="42546-110">Il cmdlet **Update-AzNetAppFilesPool** modifica un pool ANF.</span><span class="sxs-lookup"><span data-stu-id="42546-110">The **Update-AzNetAppFilesPool** cmdlet modifies an ANF pool.</span></span>

## <span data-ttu-id="42546-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="42546-111">EXAMPLES</span></span>

### <span data-ttu-id="42546-112">Esempio 1: Modificare un pool ANF</span><span class="sxs-lookup"><span data-stu-id="42546-112">Example 1: Modify an ANF pool</span></span>
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

<span data-ttu-id="42546-113">Questo comando modifica le dimensioni e QosType del pool ANF "MyAnfPool".</span><span class="sxs-lookup"><span data-stu-id="42546-113">This command changes the ANF pool "MyAnfPool" to have the given size and QosType.</span></span>

## <span data-ttu-id="42546-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="42546-114">PARAMETERS</span></span>

### <span data-ttu-id="42546-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="42546-115">-AccountName</span></span>
<span data-ttu-id="42546-116">Nome dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="42546-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="42546-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="42546-117">-AccountObject</span></span>
<span data-ttu-id="42546-118">Oggetto account contenente il pool da aggiornare</span><span class="sxs-lookup"><span data-stu-id="42546-118">The account object containing the pool to update</span></span>

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

### <span data-ttu-id="42546-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42546-119">-DefaultProfile</span></span>
<span data-ttu-id="42546-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="42546-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42546-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="42546-121">-InputObject</span></span>
<span data-ttu-id="42546-122">Oggetto pool da aggiornare</span><span class="sxs-lookup"><span data-stu-id="42546-122">The pool object to update</span></span>

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

### <span data-ttu-id="42546-123">-Location</span><span class="sxs-lookup"><span data-stu-id="42546-123">-Location</span></span>
<span data-ttu-id="42546-124">Posizione della risorsa</span><span class="sxs-lookup"><span data-stu-id="42546-124">The location of the resource</span></span>

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

### <span data-ttu-id="42546-125">-Name</span><span class="sxs-lookup"><span data-stu-id="42546-125">-Name</span></span>
<span data-ttu-id="42546-126">Nome del pool ANF</span><span class="sxs-lookup"><span data-stu-id="42546-126">The name of the ANF pool</span></span>

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

### <span data-ttu-id="42546-127">-PoolSize</span><span class="sxs-lookup"><span data-stu-id="42546-127">-PoolSize</span></span>
<span data-ttu-id="42546-128">Dimensioni del pool ANF</span><span class="sxs-lookup"><span data-stu-id="42546-128">The size of the ANF pool</span></span>

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

### <span data-ttu-id="42546-129">-QosType</span><span class="sxs-lookup"><span data-stu-id="42546-129">-QosType</span></span>
<span data-ttu-id="42546-130">Il tipo di qos della pool.</span><span class="sxs-lookup"><span data-stu-id="42546-130">The qos type of the pool.</span></span> <span data-ttu-id="42546-131">I valori possibili includono" "Auto", "Manuale"</span><span class="sxs-lookup"><span data-stu-id="42546-131">Possible values include: 'Auto', 'Manual'</span></span>

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

### <span data-ttu-id="42546-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42546-132">-ResourceGroupName</span></span>
<span data-ttu-id="42546-133">Gruppo di risorse dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="42546-133">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="42546-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="42546-134">-ResourceId</span></span>
<span data-ttu-id="42546-135">ID risorsa del pool ANF</span><span class="sxs-lookup"><span data-stu-id="42546-135">The resource id of the ANF pool</span></span>

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

### <span data-ttu-id="42546-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="42546-136">-Tag</span></span>
<span data-ttu-id="42546-137">Tabella hash che rappresenta i tag di risorsa</span><span class="sxs-lookup"><span data-stu-id="42546-137">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="42546-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="42546-138">-Confirm</span></span>
<span data-ttu-id="42546-139">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="42546-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42546-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42546-140">-WhatIf</span></span>
<span data-ttu-id="42546-141">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="42546-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42546-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="42546-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42546-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42546-143">CommonParameters</span></span>
<span data-ttu-id="42546-144">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42546-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42546-145">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="42546-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42546-146">INPUT</span><span class="sxs-lookup"><span data-stu-id="42546-146">INPUTS</span></span>

### <span data-ttu-id="42546-147">System.String</span><span class="sxs-lookup"><span data-stu-id="42546-147">System.String</span></span>

### <span data-ttu-id="42546-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="42546-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="42546-149">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="42546-149">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="42546-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="42546-150">OUTPUTS</span></span>

### <span data-ttu-id="42546-151">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="42546-151">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="42546-152">NOTE</span><span class="sxs-lookup"><span data-stu-id="42546-152">NOTES</span></span>

## <span data-ttu-id="42546-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="42546-153">RELATED LINKS</span></span>
