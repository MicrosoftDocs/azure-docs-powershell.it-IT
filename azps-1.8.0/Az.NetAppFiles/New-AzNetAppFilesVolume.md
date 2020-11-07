---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesVolume.md
ms.openlocfilehash: b742c8af0e8c36d07b2c608e74f0a02349502104
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678728"
---
# <span data-ttu-id="d7bd4-101">New-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="d7bd4-101">New-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="d7bd4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d7bd4-102">SYNOPSIS</span></span>
<span data-ttu-id="d7bd4-103">Crea un nuovo volume di file NetApp (ANF) di Azure.</span><span class="sxs-lookup"><span data-stu-id="d7bd4-103">Creates a new Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="d7bd4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d7bd4-104">SYNTAX</span></span>

### <span data-ttu-id="d7bd4-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d7bd4-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesVolume -ResourceGroupName <String> -Location <String> -AccountName <String> -PoolName <String>
 -Name <String> -UsageThreshold <Int64> -SubnetId <String> -CreationToken <String> -ServiceLevel <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7bd4-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d7bd4-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesVolume -Name <String> -UsageThreshold <Int64> -SubnetId <String> -CreationToken <String>
 -ServiceLevel <String> [-Tag <Hashtable>] -PoolObject <PSNetAppFilesPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7bd4-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d7bd4-107">DESCRIPTION</span></span>
<span data-ttu-id="d7bd4-108">Il cmdlet **New-AzNetAppFilesVolume** crea un volume di ANF.</span><span class="sxs-lookup"><span data-stu-id="d7bd4-108">The **New-AzNetAppFilesVolume** cmdlet creates an ANF volume.</span></span>

## <span data-ttu-id="d7bd4-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d7bd4-109">EXAMPLES</span></span>

### <span data-ttu-id="d7bd4-110">Esempio 1: creare un volume ANF</span><span class="sxs-lookup"><span data-stu-id="d7bd4-110">Example 1: Create an ANF volume</span></span>
```
PS C:\>New-AzNetAppFilesVolume -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume" -l "westus2" -CreationToken "MyAnfVolume" -UsageThreshold 1099511627776 -ServiceLevel "Premium" -SubnetId "/subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.Network/virtualNetworks/MyVnetName/subnets/MySubNetName"

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool/volumes/MyAnfVolume
Name              : MyAnfAccount/MyAnfPool/MyAnfVolume
Type              : Microsoft.NetApp/netAppAccounts/capacityPools/volumes
Tags              :
FileSystemId      : 3e2773a7-2a72-d003-0637-1a8b1fa3eaaf
CreationToken     : MyAnfVolume
ServiceLevel      : Premium
UsageThreshold    : 1099511627776
ProvisioningState : Succeeded
SubnetId          : /subscriptions/f557b96d-2308-4a18-aae1-b8f7e7e70cc7/resourceGroups/MyRG/providers/Microsoft.Network/virtualNetworks/MyVnetName/subnets/default
```

<span data-ttu-id="d7bd4-111">Questo comando crea il nuovo volume ANF "MyAnfVolume" nel pool "MyAnfPool".</span><span class="sxs-lookup"><span data-stu-id="d7bd4-111">This command creates the new ANF volume "MyAnfVolume" within the pool "MyAnfPool".</span></span>

## <span data-ttu-id="d7bd4-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d7bd4-112">PARAMETERS</span></span>

### <span data-ttu-id="d7bd4-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d7bd4-113">-AccountName</span></span>
<span data-ttu-id="d7bd4-114">Nome dell'account di ANF</span><span class="sxs-lookup"><span data-stu-id="d7bd4-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="d7bd4-115">-CreationToken</span><span class="sxs-lookup"><span data-stu-id="d7bd4-115">-CreationToken</span></span>
<span data-ttu-id="d7bd4-116">Percorso file univoco per il volume</span><span class="sxs-lookup"><span data-stu-id="d7bd4-116">A unique file path for the volume</span></span>

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

### <span data-ttu-id="d7bd4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7bd4-117">-DefaultProfile</span></span>
<span data-ttu-id="d7bd4-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d7bd4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7bd4-119">-Posizione</span><span class="sxs-lookup"><span data-stu-id="d7bd4-119">-Location</span></span>
<span data-ttu-id="d7bd4-120">Posizione della risorsa</span><span class="sxs-lookup"><span data-stu-id="d7bd4-120">The location of the resource</span></span>

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

### <span data-ttu-id="d7bd4-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="d7bd4-121">-Name</span></span>
<span data-ttu-id="d7bd4-122">Nome del volume di ANF</span><span class="sxs-lookup"><span data-stu-id="d7bd4-122">The name of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7bd4-123">-PoolName</span><span class="sxs-lookup"><span data-stu-id="d7bd4-123">-PoolName</span></span>
<span data-ttu-id="d7bd4-124">Nome del pool di ANF</span><span class="sxs-lookup"><span data-stu-id="d7bd4-124">The name of the ANF pool</span></span>

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

### <span data-ttu-id="d7bd4-125">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="d7bd4-125">-PoolObject</span></span>
<span data-ttu-id="d7bd4-126">Pool per il nuovo oggetto volume</span><span class="sxs-lookup"><span data-stu-id="d7bd4-126">The pool for the new volume object</span></span>

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

### <span data-ttu-id="d7bd4-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7bd4-127">-ResourceGroupName</span></span>
<span data-ttu-id="d7bd4-128">Gruppo risorse dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="d7bd4-128">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="d7bd4-129">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="d7bd4-129">-ServiceLevel</span></span>
<span data-ttu-id="d7bd4-130">Livello di servizio del volume ANF</span><span class="sxs-lookup"><span data-stu-id="d7bd4-130">The service level of the ANF volume</span></span>

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

### <span data-ttu-id="d7bd4-131">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="d7bd4-131">-SubnetId</span></span>
<span data-ttu-id="d7bd4-132">URI di risorsa di Azure per una subnet delegata</span><span class="sxs-lookup"><span data-stu-id="d7bd4-132">The Azure Resource URI for a delegated subnet</span></span>

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

### <span data-ttu-id="d7bd4-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="d7bd4-133">-Tag</span></span>
<span data-ttu-id="d7bd4-134">Hashtable che rappresenta i tag delle risorse</span><span class="sxs-lookup"><span data-stu-id="d7bd4-134">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="d7bd4-135">-UsageThreshold</span><span class="sxs-lookup"><span data-stu-id="d7bd4-135">-UsageThreshold</span></span>
<span data-ttu-id="d7bd4-136">La quota di archiviazione massima consentita per un file System in byte</span><span class="sxs-lookup"><span data-stu-id="d7bd4-136">The maximum storage quota allowed for a file system in bytes</span></span>

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

### <span data-ttu-id="d7bd4-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d7bd4-137">-Confirm</span></span>
<span data-ttu-id="d7bd4-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7bd4-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7bd4-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7bd4-139">-WhatIf</span></span>
<span data-ttu-id="d7bd4-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d7bd4-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7bd4-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d7bd4-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7bd4-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7bd4-142">CommonParameters</span></span>
<span data-ttu-id="d7bd4-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7bd4-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="d7bd4-144">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7bd4-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7bd4-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d7bd4-145">INPUTS</span></span>

### <span data-ttu-id="d7bd4-146">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="d7bd4-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="d7bd4-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d7bd4-147">OUTPUTS</span></span>

### <span data-ttu-id="d7bd4-148">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="d7bd4-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="d7bd4-149">Note</span><span class="sxs-lookup"><span data-stu-id="d7bd4-149">NOTES</span></span>

## <span data-ttu-id="d7bd4-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d7bd4-150">RELATED LINKS</span></span>
