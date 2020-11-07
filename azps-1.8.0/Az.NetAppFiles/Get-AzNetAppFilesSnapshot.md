---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilessnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesSnapshot.md
ms.openlocfilehash: 8f34145a65cde73ea1a5b925064c2b9a1d3f92a3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678737"
---
# <span data-ttu-id="cf484-101">Get-AzNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="cf484-101">Get-AzNetAppFilesSnapshot</span></span>

## <span data-ttu-id="cf484-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cf484-102">SYNOPSIS</span></span>
<span data-ttu-id="cf484-103">Ottiene i dettagli di uno snapshot di Azure NetApp file (ANF).</span><span class="sxs-lookup"><span data-stu-id="cf484-103">Gets details of an Azure NetApp Files (ANF) snapshot.</span></span>

## <span data-ttu-id="cf484-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cf484-104">SYNTAX</span></span>

### <span data-ttu-id="cf484-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cf484-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesSnapshot -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -VolumeName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cf484-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cf484-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesSnapshot [-Name <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cf484-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cf484-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesSnapshot [-Name <String>] -VolumeObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cf484-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cf484-108">DESCRIPTION</span></span>
<span data-ttu-id="cf484-109">Il cmdlet **Get-AzNetAppFilesSnapshot** ottiene i dettagli di uno snapshot ANF.</span><span class="sxs-lookup"><span data-stu-id="cf484-109">The **Get-AzNetAppFilesSnapshot** cmdlet gets details of an ANF snapshot.</span></span>

## <span data-ttu-id="cf484-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cf484-110">EXAMPLES</span></span>

### <span data-ttu-id="cf484-111">Esempio 1: ottenere uno snapshot di ANF</span><span class="sxs-lookup"><span data-stu-id="cf484-111">Example 1: Get an ANF snapshot</span></span>
```
PS C:\>Get-AzNetAppFilesSnapshot -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyAnfVolume" -Name "MyAnfSnapshot"

Output:

ResourceGroupName : MyRG
Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool/volumes/MyAnfVolume/snapshots/MyAnfSnapshot
Name              : MyAnfAccount/MyAnfPool/MyAnfVolume/MyAnfSnapshot
Type              : Microsoft.NetApp/netAppAccounts/capacityPools/volumes/snapshots
Tags              :
FileSystemId      : 3e2773a7-2a72-d003-0637-1a8b1fa3eaaf
SnapshotId        : ca7c4ebd-91cb-0e30-91f5-9154050033df
CreationDate      :
ProvisioningState : Succeeded
```

<span data-ttu-id="cf484-112">Questo comando ottiene lo snapshot denominato MyAnfSnapshot dal volume "MyAnfVolume".</span><span class="sxs-lookup"><span data-stu-id="cf484-112">This command gets the snapshot named MyAnfSnapshot from the volume "MyAnfVolume".</span></span>

## <span data-ttu-id="cf484-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cf484-113">PARAMETERS</span></span>

### <span data-ttu-id="cf484-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="cf484-114">-AccountName</span></span>
<span data-ttu-id="cf484-115">Nome dell'account di ANF</span><span class="sxs-lookup"><span data-stu-id="cf484-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="cf484-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf484-116">-DefaultProfile</span></span>
<span data-ttu-id="cf484-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cf484-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf484-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="cf484-118">-Name</span></span>
<span data-ttu-id="cf484-119">Nome dello snapshot di ANF</span><span class="sxs-lookup"><span data-stu-id="cf484-119">The name of the ANF snapshot</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SnapshotName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf484-120">-PoolName</span><span class="sxs-lookup"><span data-stu-id="cf484-120">-PoolName</span></span>
<span data-ttu-id="cf484-121">Nome del pool di ANF</span><span class="sxs-lookup"><span data-stu-id="cf484-121">The name of the ANF pool</span></span>

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

### <span data-ttu-id="cf484-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf484-122">-ResourceGroupName</span></span>
<span data-ttu-id="cf484-123">Gruppo risorse del volume ANF</span><span class="sxs-lookup"><span data-stu-id="cf484-123">The resource group of the ANF volume</span></span>

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

### <span data-ttu-id="cf484-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cf484-124">-ResourceId</span></span>
<span data-ttu-id="cf484-125">ID risorsa dello snapshot ANF</span><span class="sxs-lookup"><span data-stu-id="cf484-125">The resource id of the ANF snapshot</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf484-126">-VolumeName</span><span class="sxs-lookup"><span data-stu-id="cf484-126">-VolumeName</span></span>
<span data-ttu-id="cf484-127">Nome del volume di ANF</span><span class="sxs-lookup"><span data-stu-id="cf484-127">The name of the ANF volume</span></span>

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

### <span data-ttu-id="cf484-128">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="cf484-128">-VolumeObject</span></span>
<span data-ttu-id="cf484-129">Oggetto volume che contiene lo snapshot da restituire</span><span class="sxs-lookup"><span data-stu-id="cf484-129">The volume object containing the snapshot to return</span></span>

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

### <span data-ttu-id="cf484-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf484-130">CommonParameters</span></span>
<span data-ttu-id="cf484-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf484-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="cf484-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf484-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf484-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cf484-133">INPUTS</span></span>

### <span data-ttu-id="cf484-134">System. String</span><span class="sxs-lookup"><span data-stu-id="cf484-134">System.String</span></span>

### <span data-ttu-id="cf484-135">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="cf484-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="cf484-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cf484-136">OUTPUTS</span></span>

### <span data-ttu-id="cf484-137">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="cf484-137">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot</span></span>

## <span data-ttu-id="cf484-138">Note</span><span class="sxs-lookup"><span data-stu-id="cf484-138">NOTES</span></span>

## <span data-ttu-id="cf484-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cf484-139">RELATED LINKS</span></span>
