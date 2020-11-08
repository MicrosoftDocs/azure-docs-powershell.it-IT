---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesPool.md
ms.openlocfilehash: e63812f1972effd7956911861e5c6e07436fd4c1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94202847"
---
# <span data-ttu-id="c4f45-101">Update-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="c4f45-101">Update-AzNetAppFilesPool</span></span>

## <span data-ttu-id="c4f45-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c4f45-102">SYNOPSIS</span></span>
<span data-ttu-id="c4f45-103">Aggiorna uno Azure NetApp file (ANF) pool in base ai modificatori facoltativi forniti.</span><span class="sxs-lookup"><span data-stu-id="c4f45-103">Updates an Azure NetApp Files (ANF) pool according to the optional modifiers provided.</span></span>

## <span data-ttu-id="c4f45-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c4f45-104">SYNTAX</span></span>

### <span data-ttu-id="c4f45-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c4f45-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesPool -ResourceGroupName <String> [-Location <String>] -AccountName <String> -Name <String>
 [-PoolSize <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4f45-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4f45-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesPool -Name <String> [-PoolSize <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>]
 -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c4f45-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4f45-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesPool [-PoolSize <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4f45-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4f45-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesPool [-PoolSize <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>]
 -InputObject <PSNetAppFilesPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c4f45-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c4f45-109">DESCRIPTION</span></span>
<span data-ttu-id="c4f45-110">Il cmdlet **Update-AzNetAppFilesPool** modifica un pool di ANF.</span><span class="sxs-lookup"><span data-stu-id="c4f45-110">The **Update-AzNetAppFilesPool** cmdlet modifies an ANF pool.</span></span>

## <span data-ttu-id="c4f45-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c4f45-111">EXAMPLES</span></span>

### <span data-ttu-id="c4f45-112">Esempio 1: modificare un pool di ANF</span><span class="sxs-lookup"><span data-stu-id="c4f45-112">Example 1: Modify an ANF pool</span></span>
```
PS C:\>Update-AzNetAppFilesPool -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -PoolSize 4398046511104 -ServiceLevel "Standard"

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool
Name              : MyAnfAccount/MyAnfPool
Type              : Microsoft.NetApp/netAppAccounts/capacityPools
Tags              :
PoolId            : 9fa2ca6d-1e48-4439-30e3-7de056e44e5a
Size              : 4398046511104
ServiceLevel      : Standard
ProvisioningState : Succeeded
```

<span data-ttu-id="c4f45-113">Questo comando modifica il pool di ANF "MyAnfPool" per avere le dimensioni e il ServiceLevel specificati.</span><span class="sxs-lookup"><span data-stu-id="c4f45-113">This command changes the ANF pool "MyAnfPool" to have the given size and ServiceLevel.</span></span>

## <span data-ttu-id="c4f45-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c4f45-114">PARAMETERS</span></span>

### <span data-ttu-id="c4f45-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c4f45-115">-AccountName</span></span>
<span data-ttu-id="c4f45-116">Nome dell'account di ANF</span><span class="sxs-lookup"><span data-stu-id="c4f45-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="c4f45-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="c4f45-117">-AccountObject</span></span>
<span data-ttu-id="c4f45-118">L'oggetto account che contiene il pool da aggiornare</span><span class="sxs-lookup"><span data-stu-id="c4f45-118">The account object containing the pool to update</span></span>

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

### <span data-ttu-id="c4f45-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4f45-119">-DefaultProfile</span></span>
<span data-ttu-id="c4f45-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c4f45-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4f45-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c4f45-121">-InputObject</span></span>
<span data-ttu-id="c4f45-122">Oggetto pool da aggiornare</span><span class="sxs-lookup"><span data-stu-id="c4f45-122">The pool object to update</span></span>

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

### <span data-ttu-id="c4f45-123">-Posizione</span><span class="sxs-lookup"><span data-stu-id="c4f45-123">-Location</span></span>
<span data-ttu-id="c4f45-124">Posizione della risorsa</span><span class="sxs-lookup"><span data-stu-id="c4f45-124">The location of the resource</span></span>

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

### <span data-ttu-id="c4f45-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="c4f45-125">-Name</span></span>
<span data-ttu-id="c4f45-126">Nome del pool di ANF</span><span class="sxs-lookup"><span data-stu-id="c4f45-126">The name of the ANF pool</span></span>

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

### <span data-ttu-id="c4f45-127">-PoolSize</span><span class="sxs-lookup"><span data-stu-id="c4f45-127">-PoolSize</span></span>
<span data-ttu-id="c4f45-128">Dimensioni del pool di ANF</span><span class="sxs-lookup"><span data-stu-id="c4f45-128">The size of the ANF pool</span></span>

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

### <span data-ttu-id="c4f45-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4f45-129">-ResourceGroupName</span></span>
<span data-ttu-id="c4f45-130">Gruppo risorse dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="c4f45-130">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="c4f45-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c4f45-131">-ResourceId</span></span>
<span data-ttu-id="c4f45-132">ID risorsa del pool di ANF</span><span class="sxs-lookup"><span data-stu-id="c4f45-132">The resource id of the ANF pool</span></span>

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

### <span data-ttu-id="c4f45-133">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="c4f45-133">-ServiceLevel</span></span>
<span data-ttu-id="c4f45-134">Livello di servizio del pool di ANF</span><span class="sxs-lookup"><span data-stu-id="c4f45-134">The service level of the ANF pool</span></span>

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

### <span data-ttu-id="c4f45-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="c4f45-135">-Tag</span></span>
<span data-ttu-id="c4f45-136">Hashtable che rappresenta i tag delle risorse</span><span class="sxs-lookup"><span data-stu-id="c4f45-136">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="c4f45-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c4f45-137">-Confirm</span></span>
<span data-ttu-id="c4f45-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4f45-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4f45-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4f45-139">-WhatIf</span></span>
<span data-ttu-id="c4f45-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c4f45-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4f45-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c4f45-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4f45-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4f45-142">CommonParameters</span></span>
<span data-ttu-id="c4f45-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4f45-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4f45-144">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c4f45-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4f45-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c4f45-145">INPUTS</span></span>

### <span data-ttu-id="c4f45-146">System. String</span><span class="sxs-lookup"><span data-stu-id="c4f45-146">System.String</span></span>

### <span data-ttu-id="c4f45-147">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="c4f45-147">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="c4f45-148">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="c4f45-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="c4f45-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c4f45-149">OUTPUTS</span></span>

### <span data-ttu-id="c4f45-150">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="c4f45-150">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="c4f45-151">Note</span><span class="sxs-lookup"><span data-stu-id="c4f45-151">NOTES</span></span>

## <span data-ttu-id="c4f45-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c4f45-152">RELATED LINKS</span></span>
