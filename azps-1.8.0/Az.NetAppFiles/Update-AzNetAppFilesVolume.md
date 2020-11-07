---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesVolume.md
ms.openlocfilehash: ea943c490a87dd4c62752b97753971f0941ed3b9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678716"
---
# <span data-ttu-id="9294b-101">Update-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="9294b-101">Update-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="9294b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9294b-102">SYNOPSIS</span></span>
<span data-ttu-id="9294b-103">Aggiorna un volume di Azure NetApp file (ANF) in base ai modificatori facoltativi forniti.</span><span class="sxs-lookup"><span data-stu-id="9294b-103">Updates an Azure NetApp Files (ANF) volume according to the optional modifiers provided.</span></span>

## <span data-ttu-id="9294b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9294b-104">SYNTAX</span></span>

### <span data-ttu-id="9294b-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9294b-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesVolume -ResourceGroupName <String> -Location <String> -AccountName <String>
 -PoolName <String> -Name <String> [-UsageThreshold <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9294b-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9294b-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesVolume -Name <String> [-UsageThreshold <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>]
 -PoolObject <PSNetAppFilesPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9294b-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9294b-107">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesVolume [-UsageThreshold <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>]
 -InputObject <PSNetAppFilesVolume> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9294b-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9294b-108">DESCRIPTION</span></span>
<span data-ttu-id="9294b-109">Il cmdlet **Update-AzNetAppFilesVolume** aggiorna un volume di ANF.</span><span class="sxs-lookup"><span data-stu-id="9294b-109">The **Update-AzNetAppFilesVolume** cmdlet updates an ANF volume.</span></span>

## <span data-ttu-id="9294b-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9294b-110">EXAMPLES</span></span>

### <span data-ttu-id="9294b-111">Esempio 1: aggiornare un volume di ANF</span><span class="sxs-lookup"><span data-stu-id="9294b-111">Example 1: Update an ANF volume</span></span>
```
PS C:\>Update-AzNetAppFilesVolume -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume" -UsageThreshold Size

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool/volumes/MyAnfVolume
Name              : MyAnfAccount/MyAnfPool/MyAnfVolume
Type              : Microsoft.NetApp/netAppAccounts/capacityPools/volumes
Tags              :
FileSystemId      : 3e2773a7-2a72-d003-0637-1a8b1fa3eaaf
CreationToken     : MyAnfVolume
ServiceLevel      : Premium
UsageThreshold    : 2199023255552
ProvisioningState : Succeeded
SubnetId          : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.Network/virtualNetworks/MyRG-vnet/subnets/default
```

<span data-ttu-id="9294b-112">Questo comando Aggiorna il volume ANF "MyAnfVolume" con le nuove dimensioni di UsageThreshold.</span><span class="sxs-lookup"><span data-stu-id="9294b-112">This command updates the ANF volume "MyAnfVolume" with the new UsageThreshold size.</span></span>

## <span data-ttu-id="9294b-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9294b-113">PARAMETERS</span></span>

### <span data-ttu-id="9294b-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9294b-114">-AccountName</span></span>
<span data-ttu-id="9294b-115">Nome dell'account di ANF</span><span class="sxs-lookup"><span data-stu-id="9294b-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="9294b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9294b-116">-DefaultProfile</span></span>
<span data-ttu-id="9294b-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9294b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9294b-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9294b-118">-InputObject</span></span>
<span data-ttu-id="9294b-119">Oggetto volume da aggiornare</span><span class="sxs-lookup"><span data-stu-id="9294b-119">The volume object to update</span></span>

```yaml
Type: PSNetAppFilesVolume
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9294b-120">-Posizione</span><span class="sxs-lookup"><span data-stu-id="9294b-120">-Location</span></span>
<span data-ttu-id="9294b-121">Posizione della risorsa</span><span class="sxs-lookup"><span data-stu-id="9294b-121">The location of the resource</span></span>

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

### <span data-ttu-id="9294b-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="9294b-122">-Name</span></span>
<span data-ttu-id="9294b-123">Nome del volume di ANF</span><span class="sxs-lookup"><span data-stu-id="9294b-123">The name of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9294b-124">-PoolName</span><span class="sxs-lookup"><span data-stu-id="9294b-124">-PoolName</span></span>
<span data-ttu-id="9294b-125">Nome del pool di ANF</span><span class="sxs-lookup"><span data-stu-id="9294b-125">The name of the ANF pool</span></span>

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

### <span data-ttu-id="9294b-126">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="9294b-126">-PoolObject</span></span>
<span data-ttu-id="9294b-127">Oggetto pool che contiene il volume da aggiornare</span><span class="sxs-lookup"><span data-stu-id="9294b-127">The pool object containing the volume to update</span></span>

```yaml
Type: PSNetAppFilesPool
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9294b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9294b-128">-ResourceGroupName</span></span>
<span data-ttu-id="9294b-129">Gruppo risorse dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="9294b-129">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="9294b-130">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="9294b-130">-ServiceLevel</span></span>
<span data-ttu-id="9294b-131">Livello di servizio del volume ANF</span><span class="sxs-lookup"><span data-stu-id="9294b-131">The service level of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9294b-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="9294b-132">-Tag</span></span>
<span data-ttu-id="9294b-133">Hashtable che rappresenta i tag delle risorse</span><span class="sxs-lookup"><span data-stu-id="9294b-133">A hashtable which represents resource tags</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9294b-134">-UsageThreshold</span><span class="sxs-lookup"><span data-stu-id="9294b-134">-UsageThreshold</span></span>
<span data-ttu-id="9294b-135">La quota di archiviazione massima consentita per un file System in byte</span><span class="sxs-lookup"><span data-stu-id="9294b-135">The maximum storage quota allowed for a file system in bytes</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9294b-136">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9294b-136">-Confirm</span></span>
<span data-ttu-id="9294b-137">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9294b-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9294b-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9294b-138">-WhatIf</span></span>
<span data-ttu-id="9294b-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9294b-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9294b-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9294b-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9294b-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9294b-141">CommonParameters</span></span>
<span data-ttu-id="9294b-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9294b-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="9294b-143">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9294b-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9294b-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9294b-144">INPUTS</span></span>

### <span data-ttu-id="9294b-145">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="9294b-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="9294b-146">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="9294b-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="9294b-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9294b-147">OUTPUTS</span></span>

### <span data-ttu-id="9294b-148">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="9294b-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="9294b-149">Note</span><span class="sxs-lookup"><span data-stu-id="9294b-149">NOTES</span></span>

## <span data-ttu-id="9294b-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9294b-150">RELATED LINKS</span></span>
