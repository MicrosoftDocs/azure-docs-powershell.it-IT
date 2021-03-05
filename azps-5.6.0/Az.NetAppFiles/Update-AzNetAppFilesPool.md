---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/update-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesPool.md
ms.openlocfilehash: e8b367b724a4310eb5a3ed76bcf02e8538299845
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968110"
---
# <span data-ttu-id="9f5e7-101">Update-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="9f5e7-101">Update-AzNetAppFilesPool</span></span>

## <span data-ttu-id="9f5e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f5e7-102">SYNOPSIS</span></span>
<span data-ttu-id="9f5e7-103">Aggiorna un pool di file ANF (Azure NetApp Files) in base ai modificatori facoltativi disponibili.</span><span class="sxs-lookup"><span data-stu-id="9f5e7-103">Updates an Azure NetApp Files (ANF) pool according to the optional modifiers provided.</span></span>

## <span data-ttu-id="9f5e7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9f5e7-104">SYNTAX</span></span>

### <span data-ttu-id="9f5e7-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9f5e7-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesPool -ResourceGroupName <String> [-Location <String>] -AccountName <String> -Name <String>
 [-PoolSize <Int64>] [-QosType <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f5e7-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f5e7-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesPool -Name <String> [-PoolSize <Int64>] [-QosType <String>] [-Tag <Hashtable>]
 -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9f5e7-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f5e7-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesPool [-PoolSize <Int64>] [-QosType <String>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f5e7-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f5e7-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesPool [-PoolSize <Int64>] [-QosType <String>] [-Tag <Hashtable>]
 -InputObject <PSNetAppFilesPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9f5e7-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9f5e7-109">DESCRIPTION</span></span>
<span data-ttu-id="9f5e7-110">Il cmdlet **Update-AzNetAppFilesPool** modifica un pool ANF.</span><span class="sxs-lookup"><span data-stu-id="9f5e7-110">The **Update-AzNetAppFilesPool** cmdlet modifies an ANF pool.</span></span>

## <span data-ttu-id="9f5e7-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9f5e7-111">EXAMPLES</span></span>

### <span data-ttu-id="9f5e7-112">Esempio 1: Modificare un pool ANF</span><span class="sxs-lookup"><span data-stu-id="9f5e7-112">Example 1: Modify an ANF pool</span></span>
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

<span data-ttu-id="9f5e7-113">Questo comando modifica le dimensioni e QosType del pool ANF "MyAnfPool".</span><span class="sxs-lookup"><span data-stu-id="9f5e7-113">This command changes the ANF pool "MyAnfPool" to have the given size and QosType.</span></span>

## <span data-ttu-id="9f5e7-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9f5e7-114">PARAMETERS</span></span>

### <span data-ttu-id="9f5e7-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9f5e7-115">-AccountName</span></span>
<span data-ttu-id="9f5e7-116">Nome dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="9f5e7-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="9f5e7-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="9f5e7-117">-AccountObject</span></span>
<span data-ttu-id="9f5e7-118">Oggetto account contenente il pool da aggiornare</span><span class="sxs-lookup"><span data-stu-id="9f5e7-118">The account object containing the pool to update</span></span>

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

### <span data-ttu-id="9f5e7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f5e7-119">-DefaultProfile</span></span>
<span data-ttu-id="9f5e7-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9f5e7-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f5e7-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9f5e7-121">-InputObject</span></span>
<span data-ttu-id="9f5e7-122">Oggetto pool da aggiornare</span><span class="sxs-lookup"><span data-stu-id="9f5e7-122">The pool object to update</span></span>

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

### <span data-ttu-id="9f5e7-123">-Location</span><span class="sxs-lookup"><span data-stu-id="9f5e7-123">-Location</span></span>
<span data-ttu-id="9f5e7-124">Posizione della risorsa</span><span class="sxs-lookup"><span data-stu-id="9f5e7-124">The location of the resource</span></span>

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

### <span data-ttu-id="9f5e7-125">-Name</span><span class="sxs-lookup"><span data-stu-id="9f5e7-125">-Name</span></span>
<span data-ttu-id="9f5e7-126">Nome del pool ANF</span><span class="sxs-lookup"><span data-stu-id="9f5e7-126">The name of the ANF pool</span></span>

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

### <span data-ttu-id="9f5e7-127">-PoolSize</span><span class="sxs-lookup"><span data-stu-id="9f5e7-127">-PoolSize</span></span>
<span data-ttu-id="9f5e7-128">Dimensioni del pool ANF</span><span class="sxs-lookup"><span data-stu-id="9f5e7-128">The size of the ANF pool</span></span>

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

### <span data-ttu-id="9f5e7-129">-QosType</span><span class="sxs-lookup"><span data-stu-id="9f5e7-129">-QosType</span></span>
<span data-ttu-id="9f5e7-130">Il tipo di qos della pool.</span><span class="sxs-lookup"><span data-stu-id="9f5e7-130">The qos type of the pool.</span></span> <span data-ttu-id="9f5e7-131">I valori possibili includono" "Auto", "Manuale"</span><span class="sxs-lookup"><span data-stu-id="9f5e7-131">Possible values include: 'Auto', 'Manual'</span></span>

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

### <span data-ttu-id="9f5e7-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f5e7-132">-ResourceGroupName</span></span>
<span data-ttu-id="9f5e7-133">Gruppo di risorse dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="9f5e7-133">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="9f5e7-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9f5e7-134">-ResourceId</span></span>
<span data-ttu-id="9f5e7-135">ID risorsa del pool ANF</span><span class="sxs-lookup"><span data-stu-id="9f5e7-135">The resource id of the ANF pool</span></span>

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

### <span data-ttu-id="9f5e7-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="9f5e7-136">-Tag</span></span>
<span data-ttu-id="9f5e7-137">Tabella hash che rappresenta i tag di risorsa</span><span class="sxs-lookup"><span data-stu-id="9f5e7-137">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="9f5e7-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9f5e7-138">-Confirm</span></span>
<span data-ttu-id="9f5e7-139">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9f5e7-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f5e7-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f5e7-140">-WhatIf</span></span>
<span data-ttu-id="9f5e7-141">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9f5e7-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f5e7-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9f5e7-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f5e7-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f5e7-143">CommonParameters</span></span>
<span data-ttu-id="9f5e7-144">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f5e7-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f5e7-145">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9f5e7-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f5e7-146">INPUT</span><span class="sxs-lookup"><span data-stu-id="9f5e7-146">INPUTS</span></span>

### <span data-ttu-id="9f5e7-147">System.String</span><span class="sxs-lookup"><span data-stu-id="9f5e7-147">System.String</span></span>

### <span data-ttu-id="9f5e7-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="9f5e7-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="9f5e7-149">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="9f5e7-149">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="9f5e7-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9f5e7-150">OUTPUTS</span></span>

### <span data-ttu-id="9f5e7-151">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="9f5e7-151">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="9f5e7-152">NOTE</span><span class="sxs-lookup"><span data-stu-id="9f5e7-152">NOTES</span></span>

## <span data-ttu-id="9f5e7-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9f5e7-153">RELATED LINKS</span></span>
