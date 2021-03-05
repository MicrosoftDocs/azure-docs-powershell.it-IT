---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/get-aznetappfilessnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesSnapshot.md
ms.openlocfilehash: 80d8a27aaf0d2aa27f9924d93669548c1d0dda93
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968590"
---
# <span data-ttu-id="5b3dd-101">Get-AzNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="5b3dd-101">Get-AzNetAppFilesSnapshot</span></span>

## <span data-ttu-id="5b3dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b3dd-102">SYNOPSIS</span></span>
<span data-ttu-id="5b3dd-103">Recupera i dettagli di uno snapshot dei file ANF di Azure NetApp.</span><span class="sxs-lookup"><span data-stu-id="5b3dd-103">Gets details of an Azure NetApp Files (ANF) snapshot.</span></span>

## <span data-ttu-id="5b3dd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5b3dd-104">SYNTAX</span></span>

### <span data-ttu-id="5b3dd-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5b3dd-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesSnapshot -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -VolumeName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5b3dd-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b3dd-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesSnapshot [-Name <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5b3dd-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b3dd-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesSnapshot [-Name <String>] -VolumeObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b3dd-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5b3dd-108">DESCRIPTION</span></span>
<span data-ttu-id="5b3dd-109">Il cmdlet **Get-AzNetAppFilesSnapshot** ottiene i dettagli di uno snapshot ANF.</span><span class="sxs-lookup"><span data-stu-id="5b3dd-109">The **Get-AzNetAppFilesSnapshot** cmdlet gets details of an ANF snapshot.</span></span>

## <span data-ttu-id="5b3dd-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5b3dd-110">EXAMPLES</span></span>

### <span data-ttu-id="5b3dd-111">Esempio 1: Ottenere uno snapshot ANF</span><span class="sxs-lookup"><span data-stu-id="5b3dd-111">Example 1: Get an ANF snapshot</span></span>
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
Created           :
ProvisioningState : Succeeded
```

<span data-ttu-id="5b3dd-112">Questo comando recupera lo snapshot denominato MyAnfSnapshot dal volume "MyAnfVolume".</span><span class="sxs-lookup"><span data-stu-id="5b3dd-112">This command gets the snapshot named MyAnfSnapshot from the volume "MyAnfVolume".</span></span>

## <span data-ttu-id="5b3dd-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5b3dd-113">PARAMETERS</span></span>

### <span data-ttu-id="5b3dd-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5b3dd-114">-AccountName</span></span>
<span data-ttu-id="5b3dd-115">Nome dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="5b3dd-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="5b3dd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b3dd-116">-DefaultProfile</span></span>
<span data-ttu-id="5b3dd-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5b3dd-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b3dd-118">-Name</span><span class="sxs-lookup"><span data-stu-id="5b3dd-118">-Name</span></span>
<span data-ttu-id="5b3dd-119">Nome dello snapshot ANF</span><span class="sxs-lookup"><span data-stu-id="5b3dd-119">The name of the ANF snapshot</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SnapshotName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b3dd-120">-PoolName</span><span class="sxs-lookup"><span data-stu-id="5b3dd-120">-PoolName</span></span>
<span data-ttu-id="5b3dd-121">Nome del pool ANF</span><span class="sxs-lookup"><span data-stu-id="5b3dd-121">The name of the ANF pool</span></span>

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

### <span data-ttu-id="5b3dd-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b3dd-122">-ResourceGroupName</span></span>
<span data-ttu-id="5b3dd-123">Gruppo di risorse del volume ANF</span><span class="sxs-lookup"><span data-stu-id="5b3dd-123">The resource group of the ANF volume</span></span>

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

### <span data-ttu-id="5b3dd-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5b3dd-124">-ResourceId</span></span>
<span data-ttu-id="5b3dd-125">ID risorsa dello snapshot ANF</span><span class="sxs-lookup"><span data-stu-id="5b3dd-125">The resource id of the ANF snapshot</span></span>

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

### <span data-ttu-id="5b3dd-126">-VolumeName</span><span class="sxs-lookup"><span data-stu-id="5b3dd-126">-VolumeName</span></span>
<span data-ttu-id="5b3dd-127">Nome del volume ANF</span><span class="sxs-lookup"><span data-stu-id="5b3dd-127">The name of the ANF volume</span></span>

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

### <span data-ttu-id="5b3dd-128">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="5b3dd-128">-VolumeObject</span></span>
<span data-ttu-id="5b3dd-129">Oggetto volume contenente lo snapshot da restituire</span><span class="sxs-lookup"><span data-stu-id="5b3dd-129">The volume object containing the snapshot to return</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5b3dd-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b3dd-130">CommonParameters</span></span>
<span data-ttu-id="5b3dd-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b3dd-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b3dd-132">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5b3dd-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b3dd-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="5b3dd-133">INPUTS</span></span>

### <span data-ttu-id="5b3dd-134">System.String</span><span class="sxs-lookup"><span data-stu-id="5b3dd-134">System.String</span></span>

### <span data-ttu-id="5b3dd-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="5b3dd-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="5b3dd-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5b3dd-136">OUTPUTS</span></span>

### <span data-ttu-id="5b3dd-137">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="5b3dd-137">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot</span></span>

## <span data-ttu-id="5b3dd-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="5b3dd-138">NOTES</span></span>

## <span data-ttu-id="5b3dd-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5b3dd-139">RELATED LINKS</span></span>
