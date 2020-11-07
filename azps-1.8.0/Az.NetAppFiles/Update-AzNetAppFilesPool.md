---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesPool.md
ms.openlocfilehash: 3dd02a2dc0cf7090ba2711b6155d25038397ab9e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678717"
---
# <span data-ttu-id="61573-101">Update-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="61573-101">Update-AzNetAppFilesPool</span></span>

## <span data-ttu-id="61573-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="61573-102">SYNOPSIS</span></span>
<span data-ttu-id="61573-103">Aggiorna un pool di file di Azure NetApp (ANF) con il nuovo set di dati.</span><span class="sxs-lookup"><span data-stu-id="61573-103">Updates an Azure NetApp Files (ANF) pool with the new data set.</span></span>

## <span data-ttu-id="61573-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="61573-104">SYNTAX</span></span>

### <span data-ttu-id="61573-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="61573-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesPool -ResourceGroupName <String> -Location <String> -AccountName <String> -Name <String>
 -PoolSize <Int64> -ServiceLevel <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="61573-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="61573-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesPool -Name <String> -PoolSize <Int64> -ServiceLevel <String>
 -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="61573-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="61573-107">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesPool -PoolSize <Int64> -ServiceLevel <String> -InputObject <PSNetAppFilesPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61573-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="61573-108">DESCRIPTION</span></span>
<span data-ttu-id="61573-109">Il cmdlet **Update-AzNetAppFilesPool** modifica un pool di ANF.</span><span class="sxs-lookup"><span data-stu-id="61573-109">The **Update-AzNetAppFilesPool** cmdlet modifies an ANF pool.</span></span>

## <span data-ttu-id="61573-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="61573-110">EXAMPLES</span></span>

### <span data-ttu-id="61573-111">Esempio 1: modificare un pool di ANF</span><span class="sxs-lookup"><span data-stu-id="61573-111">Example 1: Modify an ANF pool</span></span>
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

<span data-ttu-id="61573-112">Questo comando modifica il pool di ANF "MyAnfPool" per avere le dimensioni e il ServiceLevel specificati.</span><span class="sxs-lookup"><span data-stu-id="61573-112">This command changes the ANF pool "MyAnfPool" to have the given size and ServiceLevel.</span></span>

## <span data-ttu-id="61573-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="61573-113">PARAMETERS</span></span>

### <span data-ttu-id="61573-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="61573-114">-AccountName</span></span>
<span data-ttu-id="61573-115">Nome dell'account di ANF</span><span class="sxs-lookup"><span data-stu-id="61573-115">The name of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61573-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="61573-116">-AccountObject</span></span>
<span data-ttu-id="61573-117">L'oggetto account che contiene il pool da aggiornare</span><span class="sxs-lookup"><span data-stu-id="61573-117">The account object containing the pool to update</span></span>

```yaml
Type: PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="61573-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61573-118">-DefaultProfile</span></span>
<span data-ttu-id="61573-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="61573-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61573-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="61573-120">-InputObject</span></span>
<span data-ttu-id="61573-121">Oggetto pool da aggiornare</span><span class="sxs-lookup"><span data-stu-id="61573-121">The pool object to update</span></span>

```yaml
Type: PSNetAppFilesPool
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="61573-122">-Posizione</span><span class="sxs-lookup"><span data-stu-id="61573-122">-Location</span></span>
<span data-ttu-id="61573-123">Posizione della risorsa</span><span class="sxs-lookup"><span data-stu-id="61573-123">The location of the resource</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61573-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="61573-124">-Name</span></span>
<span data-ttu-id="61573-125">Nome del pool di ANF</span><span class="sxs-lookup"><span data-stu-id="61573-125">The name of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: PoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61573-126">-PoolSize</span><span class="sxs-lookup"><span data-stu-id="61573-126">-PoolSize</span></span>
<span data-ttu-id="61573-127">Dimensioni del pool di ANF</span><span class="sxs-lookup"><span data-stu-id="61573-127">The size of the ANF pool</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61573-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61573-128">-ResourceGroupName</span></span>
<span data-ttu-id="61573-129">Gruppo risorse dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="61573-129">The resource group of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61573-130">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="61573-130">-ServiceLevel</span></span>
<span data-ttu-id="61573-131">Livello di servizio del pool di ANF</span><span class="sxs-lookup"><span data-stu-id="61573-131">The service level of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61573-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="61573-132">-Confirm</span></span>
<span data-ttu-id="61573-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61573-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61573-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61573-134">-WhatIf</span></span>
<span data-ttu-id="61573-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="61573-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61573-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="61573-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61573-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61573-137">CommonParameters</span></span>
<span data-ttu-id="61573-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61573-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="61573-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61573-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61573-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="61573-140">INPUTS</span></span>

### <span data-ttu-id="61573-141">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="61573-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="61573-142">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="61573-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="61573-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="61573-143">OUTPUTS</span></span>

### <span data-ttu-id="61573-144">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="61573-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="61573-145">Note</span><span class="sxs-lookup"><span data-stu-id="61573-145">NOTES</span></span>

## <span data-ttu-id="61573-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="61573-146">RELATED LINKS</span></span>
