---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesVolume.md
ms.openlocfilehash: 3d44c9def7dd56fa0d3fa58fd417a738c5db051b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678736"
---
# <span data-ttu-id="5add9-101">Get-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="5add9-101">Get-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="5add9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5add9-102">SYNOPSIS</span></span>
<span data-ttu-id="5add9-103">Ottiene i dettagli di un volume di Azure NetApp file (ANF).</span><span class="sxs-lookup"><span data-stu-id="5add9-103">Gets details of an Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="5add9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5add9-104">SYNTAX</span></span>

### <span data-ttu-id="5add9-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5add9-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesVolume -ResourceGroupName <String> -AccountName <String> -PoolName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5add9-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5add9-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesVolume -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5add9-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5add9-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesVolume -PoolObject <PSNetAppFilesPool> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5add9-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5add9-108">DESCRIPTION</span></span>
<span data-ttu-id="5add9-109">Il cmdlet **Get-AzNetAppFilesVolume** ottiene i dettagli di un volume di ANF.</span><span class="sxs-lookup"><span data-stu-id="5add9-109">The **Get-AzNetAppFilesVolume** cmdlet gets details of an ANF volume.</span></span>

## <span data-ttu-id="5add9-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5add9-110">EXAMPLES</span></span>

### <span data-ttu-id="5add9-111">Esempio 1: ottenere un volume ANF</span><span class="sxs-lookup"><span data-stu-id="5add9-111">Example 1: Get an ANF volume</span></span>
```
PS C:\>Get-AzNetAppFilesVolume -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume"

Output:

ResourceGroupName : MyRG
Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool/volumes/MyAnfVolume
Name              : MyAnfAccount/MyAnfPool/MyAnfVolume
Type              : Microsoft.NetApp/netAppAccounts/capacityPools/volumes
Tags              :
FileSystemId      : 3e2773a7-2a72-d003-0637-1a8b1fa3eaaf
CreationToken     :
ServiceLevel      : Premium
UsageThreshold    : 1099511627776
ProvisioningState : Succeeded
SubnetId          : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.Network/virtualNetworks/MyRG-vnet/subnets/default
```

<span data-ttu-id="5add9-112">Questo comando ottiene il volume denominato MyAnfVolume dal pool "MyAnfPool".</span><span class="sxs-lookup"><span data-stu-id="5add9-112">This command gets the volume named MyAnfVolume from the pool "MyAnfPool".</span></span> 

## <span data-ttu-id="5add9-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5add9-113">PARAMETERS</span></span>

### <span data-ttu-id="5add9-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5add9-114">-AccountName</span></span>
<span data-ttu-id="5add9-115">Nome dell'account di ANF</span><span class="sxs-lookup"><span data-stu-id="5add9-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="5add9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5add9-116">-DefaultProfile</span></span>
<span data-ttu-id="5add9-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5add9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5add9-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="5add9-118">-Name</span></span>
<span data-ttu-id="5add9-119">Nome del volume di ANF</span><span class="sxs-lookup"><span data-stu-id="5add9-119">The name of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: VolumeName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5add9-120">-PoolName</span><span class="sxs-lookup"><span data-stu-id="5add9-120">-PoolName</span></span>
<span data-ttu-id="5add9-121">Nome del pool di ANF</span><span class="sxs-lookup"><span data-stu-id="5add9-121">The name of the ANF pool</span></span>

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

### <span data-ttu-id="5add9-122">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="5add9-122">-PoolObject</span></span>
<span data-ttu-id="5add9-123">Oggetto pool che contiene il volume da restituire</span><span class="sxs-lookup"><span data-stu-id="5add9-123">The pool object containing the volume to return</span></span>

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

### <span data-ttu-id="5add9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5add9-124">-ResourceGroupName</span></span>
<span data-ttu-id="5add9-125">Gruppo risorse del volume ANF</span><span class="sxs-lookup"><span data-stu-id="5add9-125">The resource group of the ANF volume</span></span>

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

### <span data-ttu-id="5add9-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5add9-126">-ResourceId</span></span>
<span data-ttu-id="5add9-127">ID risorsa del volume ANF</span><span class="sxs-lookup"><span data-stu-id="5add9-127">The resource id of the ANF volume</span></span>

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

### <span data-ttu-id="5add9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5add9-128">CommonParameters</span></span>
<span data-ttu-id="5add9-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5add9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="5add9-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5add9-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5add9-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5add9-131">INPUTS</span></span>

### <span data-ttu-id="5add9-132">System. String</span><span class="sxs-lookup"><span data-stu-id="5add9-132">System.String</span></span>

### <span data-ttu-id="5add9-133">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="5add9-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="5add9-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5add9-134">OUTPUTS</span></span>

### <span data-ttu-id="5add9-135">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="5add9-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="5add9-136">Note</span><span class="sxs-lookup"><span data-stu-id="5add9-136">NOTES</span></span>

## <span data-ttu-id="5add9-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5add9-137">RELATED LINKS</span></span>
