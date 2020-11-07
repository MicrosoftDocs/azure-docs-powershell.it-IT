---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesVolume.md
ms.openlocfilehash: cad30d489b53ccfd9f45cbc619ce4384cc904903
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93853421"
---
# <span data-ttu-id="b5fa7-101">New-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="b5fa7-101">New-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="b5fa7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b5fa7-102">SYNOPSIS</span></span>
<span data-ttu-id="b5fa7-103">Crea un nuovo volume di file NetApp (ANF) di Azure.</span><span class="sxs-lookup"><span data-stu-id="b5fa7-103">Creates a new Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="b5fa7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b5fa7-104">SYNTAX</span></span>

### <span data-ttu-id="b5fa7-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b5fa7-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesVolume -ResourceGroupName <String> -Location <String> -AccountName <String> -PoolName <String>
 -Name <String> -UsageThreshold <Int64> -SubnetId <String> -CreationToken <String> -ServiceLevel <String>
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>]
 [-ProtocolType <System.String[]>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5fa7-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b5fa7-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesVolume -Name <String> -UsageThreshold <Int64> -SubnetId <String> -CreationToken <String>
 -ServiceLevel <String> [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>]
 [-ProtocolType <System.String[]>]
 [-Tag <Hashtable>] -PoolObject <PSNetAppFilesPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5fa7-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b5fa7-107">DESCRIPTION</span></span>
<span data-ttu-id="b5fa7-108">Il cmdlet **New-AzNetAppFilesVolume** crea un volume di ANF.</span><span class="sxs-lookup"><span data-stu-id="b5fa7-108">The **New-AzNetAppFilesVolume** cmdlet creates an ANF volume.</span></span>

## <span data-ttu-id="b5fa7-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b5fa7-109">EXAMPLES</span></span>

### <span data-ttu-id="b5fa7-110">Esempio 1: creare un volume ANF</span><span class="sxs-lookup"><span data-stu-id="b5fa7-110">Example 1: Create an ANF volume</span></span>
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

<span data-ttu-id="b5fa7-111">Questo comando crea il nuovo volume ANF "MyAnfVolume" nel pool "MyAnfPool".</span><span class="sxs-lookup"><span data-stu-id="b5fa7-111">This command creates the new ANF volume "MyAnfVolume" within the pool "MyAnfPool".</span></span>

## <span data-ttu-id="b5fa7-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b5fa7-112">PARAMETERS</span></span>

### <span data-ttu-id="b5fa7-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b5fa7-113">-AccountName</span></span>
<span data-ttu-id="b5fa7-114">Nome dell'account di ANF</span><span class="sxs-lookup"><span data-stu-id="b5fa7-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="b5fa7-115">-CreationToken</span><span class="sxs-lookup"><span data-stu-id="b5fa7-115">-CreationToken</span></span>
<span data-ttu-id="b5fa7-116">Percorso file univoco per il volume</span><span class="sxs-lookup"><span data-stu-id="b5fa7-116">A unique file path for the volume</span></span>

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

### <span data-ttu-id="b5fa7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5fa7-117">-DefaultProfile</span></span>
<span data-ttu-id="b5fa7-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b5fa7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5fa7-119">-ExportPolicy</span><span class="sxs-lookup"><span data-stu-id="b5fa7-119">-ExportPolicy</span></span>
<span data-ttu-id="b5fa7-120">Matrice Hashtable che rappresenta i criteri di esportazione</span><span class="sxs-lookup"><span data-stu-id="b5fa7-120">A hashtable array which represents the export policy</span></span>

```yaml
Type: PSNetAppFilesVolumeExportPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5fa7-121">-Posizione</span><span class="sxs-lookup"><span data-stu-id="b5fa7-121">-Location</span></span>
<span data-ttu-id="b5fa7-122">Posizione della risorsa</span><span class="sxs-lookup"><span data-stu-id="b5fa7-122">The location of the resource</span></span>

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

### <span data-ttu-id="b5fa7-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="b5fa7-123">-Name</span></span>
<span data-ttu-id="b5fa7-124">Nome del volume di ANF</span><span class="sxs-lookup"><span data-stu-id="b5fa7-124">The name of the ANF volume</span></span>

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

### <span data-ttu-id="b5fa7-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="b5fa7-125">-PoolName</span></span>
<span data-ttu-id="b5fa7-126">Nome del pool di ANF</span><span class="sxs-lookup"><span data-stu-id="b5fa7-126">The name of the ANF pool</span></span>

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

### <span data-ttu-id="b5fa7-127">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="b5fa7-127">-PoolObject</span></span>
<span data-ttu-id="b5fa7-128">Pool per il nuovo oggetto volume</span><span class="sxs-lookup"><span data-stu-id="b5fa7-128">The pool for the new volume object</span></span>

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

### <span data-ttu-id="b5fa7-129">-ProtocolType</span><span class="sxs-lookup"><span data-stu-id="b5fa7-129">-ProtocolType</span></span>
<span data-ttu-id="b5fa7-130">Matrice Hashtable che rappresenta i criteri di esportazione</span><span class="sxs-lookup"><span data-stu-id="b5fa7-130">A hashtable array which represents the export policy</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5fa7-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5fa7-131">-ResourceGroupName</span></span>
<span data-ttu-id="b5fa7-132">Gruppo risorse dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="b5fa7-132">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="b5fa7-133">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="b5fa7-133">-ServiceLevel</span></span>
<span data-ttu-id="b5fa7-134">Livello di servizio del volume ANF</span><span class="sxs-lookup"><span data-stu-id="b5fa7-134">The service level of the ANF volume</span></span>

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

```yaml
Type: String
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5fa7-135">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="b5fa7-135">-SubnetId</span></span>
<span data-ttu-id="b5fa7-136">URI di risorsa di Azure per una subnet delegata</span><span class="sxs-lookup"><span data-stu-id="b5fa7-136">The Azure Resource URI for a delegated subnet</span></span>

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

### <span data-ttu-id="b5fa7-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="b5fa7-137">-Tag</span></span>
<span data-ttu-id="b5fa7-138">Hashtable che rappresenta i tag delle risorse</span><span class="sxs-lookup"><span data-stu-id="b5fa7-138">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="b5fa7-139">-UsageThreshold</span><span class="sxs-lookup"><span data-stu-id="b5fa7-139">-UsageThreshold</span></span>
<span data-ttu-id="b5fa7-140">La quota di archiviazione massima consentita per un file System in byte</span><span class="sxs-lookup"><span data-stu-id="b5fa7-140">The maximum storage quota allowed for a file system in bytes</span></span>

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

### <span data-ttu-id="b5fa7-141">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b5fa7-141">-Confirm</span></span>
<span data-ttu-id="b5fa7-142">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5fa7-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5fa7-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5fa7-143">-WhatIf</span></span>
<span data-ttu-id="b5fa7-144">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b5fa7-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5fa7-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b5fa7-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5fa7-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5fa7-146">CommonParameters</span></span>
<span data-ttu-id="b5fa7-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5fa7-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="b5fa7-148">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5fa7-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5fa7-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b5fa7-149">INPUTS</span></span>

### <span data-ttu-id="b5fa7-150">System. String</span><span class="sxs-lookup"><span data-stu-id="b5fa7-150">System.String</span></span>

### <span data-ttu-id="b5fa7-151">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="b5fa7-151">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="b5fa7-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b5fa7-152">OUTPUTS</span></span>

### <span data-ttu-id="b5fa7-153">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="b5fa7-153">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="b5fa7-154">Note</span><span class="sxs-lookup"><span data-stu-id="b5fa7-154">NOTES</span></span>

## <span data-ttu-id="b5fa7-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b5fa7-155">RELATED LINKS</span></span>
