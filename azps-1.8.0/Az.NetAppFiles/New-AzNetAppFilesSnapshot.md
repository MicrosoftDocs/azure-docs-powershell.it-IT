---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilessnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesSnapshot.md
ms.openlocfilehash: bad4c1dfc2317bcc4d03414980cafa73c78949d2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678729"
---
# <span data-ttu-id="a06d1-101">New-AzNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="a06d1-101">New-AzNetAppFilesSnapshot</span></span>

## <span data-ttu-id="a06d1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a06d1-102">SYNOPSIS</span></span>
<span data-ttu-id="a06d1-103">Crea un nuovo snapshot di ANF (Azure NetApp files).</span><span class="sxs-lookup"><span data-stu-id="a06d1-103">Creates a new Azure NetApp Files (ANF) snapshot.</span></span>

## <span data-ttu-id="a06d1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a06d1-104">SYNTAX</span></span>

### <span data-ttu-id="a06d1-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a06d1-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesSnapshot -ResourceGroupName <String> -Location <String> -AccountName <String>
 -PoolName <String> -VolumeName <String> -Name <String> -FileSystemId <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a06d1-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a06d1-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesSnapshot -Name <String> [-Tag <Hashtable>] -VolumeObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a06d1-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a06d1-107">DESCRIPTION</span></span>
<span data-ttu-id="a06d1-108">Il cmdlet **New-AzNetAppFilesSnapshot** crea uno snapshot ANF.</span><span class="sxs-lookup"><span data-stu-id="a06d1-108">The **New-AzNetAppFilesSnapshot** cmdlet creates an ANF snapshot.</span></span>

## <span data-ttu-id="a06d1-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a06d1-109">EXAMPLES</span></span>

### <span data-ttu-id="a06d1-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a06d1-110">Example 1</span></span>
```
PS C:\>New-AzNetAppFilesSnapshot -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyAnfVolume" -SnapshotName "MyAnfSnapshot" -FileSystemId "3e2773a7-2a72-d003-0637-1a8b1fa3eaaf"

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool/volumes/MyAnfVolume/snapshots/MyAnfSnapshot
Name              : MyAnfAccount/MyAnfPool/MyAnfVolume/MyAnfSnapshot
Type              : Microsoft.NetApp/netAppAccounts/capacityPools/volumes/snapshots
Tags              :
SnapshotId        : ca7c4ebd-91cb-0e30-91f5-9154050033df
FileSystemId      : 3e2773a7-2a72-d003-0637-1a8b1fa3eaaf
CreationDate      :
ProvisioningState : Succeeded
```

<span data-ttu-id="a06d1-111">Questo comando crea il nuovo snapshot ANF "MyAnfSnapshot" nel volume "MyAnfVolume".</span><span class="sxs-lookup"><span data-stu-id="a06d1-111">This command creates the new ANF snapshot "MyAnfSnapshot" within the volume "MyAnfVolume".</span></span>

## <span data-ttu-id="a06d1-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a06d1-112">PARAMETERS</span></span>

### <span data-ttu-id="a06d1-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a06d1-113">-AccountName</span></span>
<span data-ttu-id="a06d1-114">Nome dell'account di ANF</span><span class="sxs-lookup"><span data-stu-id="a06d1-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="a06d1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a06d1-115">-DefaultProfile</span></span>
<span data-ttu-id="a06d1-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a06d1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a06d1-117">-FileSystemId</span><span class="sxs-lookup"><span data-stu-id="a06d1-117">-FileSystemId</span></span>
<span data-ttu-id="a06d1-118">ID file System</span><span class="sxs-lookup"><span data-stu-id="a06d1-118">The file system id</span></span>

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

### <span data-ttu-id="a06d1-119">-Posizione</span><span class="sxs-lookup"><span data-stu-id="a06d1-119">-Location</span></span>
<span data-ttu-id="a06d1-120">Posizione della risorsa</span><span class="sxs-lookup"><span data-stu-id="a06d1-120">The location of the resource</span></span>

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

### <span data-ttu-id="a06d1-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="a06d1-121">-Name</span></span>
<span data-ttu-id="a06d1-122">Nome dello snapshot di ANF</span><span class="sxs-lookup"><span data-stu-id="a06d1-122">The name of the ANF snapshot</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SnapshotName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a06d1-123">-PoolName</span><span class="sxs-lookup"><span data-stu-id="a06d1-123">-PoolName</span></span>
<span data-ttu-id="a06d1-124">Nome del pool di ANF</span><span class="sxs-lookup"><span data-stu-id="a06d1-124">The name of the ANF pool</span></span>

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

### <span data-ttu-id="a06d1-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a06d1-125">-ResourceGroupName</span></span>
<span data-ttu-id="a06d1-126">Gruppo risorse dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="a06d1-126">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="a06d1-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="a06d1-127">-Tag</span></span>
<span data-ttu-id="a06d1-128">Hashtable che rappresenta i tag delle risorse</span><span class="sxs-lookup"><span data-stu-id="a06d1-128">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="a06d1-129">-VolumeName</span><span class="sxs-lookup"><span data-stu-id="a06d1-129">-VolumeName</span></span>
<span data-ttu-id="a06d1-130">Nome del volume di ANF</span><span class="sxs-lookup"><span data-stu-id="a06d1-130">The name of the ANF volume</span></span>

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

### <span data-ttu-id="a06d1-131">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="a06d1-131">-VolumeObject</span></span>
<span data-ttu-id="a06d1-132">Il volume per il nuovo oggetto snapshot</span><span class="sxs-lookup"><span data-stu-id="a06d1-132">The volume for the new snapshot object</span></span>

```yaml
Type: PSNetAppFilesVolume
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a06d1-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a06d1-133">-Confirm</span></span>
<span data-ttu-id="a06d1-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a06d1-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a06d1-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a06d1-135">-WhatIf</span></span>
<span data-ttu-id="a06d1-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a06d1-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a06d1-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a06d1-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a06d1-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a06d1-138">CommonParameters</span></span>
<span data-ttu-id="a06d1-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a06d1-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="a06d1-140">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a06d1-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a06d1-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a06d1-141">INPUTS</span></span>

### <span data-ttu-id="a06d1-142">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="a06d1-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="a06d1-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a06d1-143">OUTPUTS</span></span>

### <span data-ttu-id="a06d1-144">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="a06d1-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot</span></span>

## <span data-ttu-id="a06d1-145">Note</span><span class="sxs-lookup"><span data-stu-id="a06d1-145">NOTES</span></span>

## <span data-ttu-id="a06d1-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a06d1-146">RELATED LINKS</span></span>