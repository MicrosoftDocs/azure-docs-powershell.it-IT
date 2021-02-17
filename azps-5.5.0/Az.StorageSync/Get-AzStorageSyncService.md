---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncService.md
ms.openlocfilehash: ec446a92c96bd92d7a4af5610f00ff76dcd50b50
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190678"
---
# <span data-ttu-id="cd268-101">Get-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="cd268-101">Get-AzStorageSyncService</span></span>

## <span data-ttu-id="cd268-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd268-102">SYNOPSIS</span></span>
<span data-ttu-id="cd268-103">Questo comando elenca tutti i servizi di sincronizzazione di archiviazione in un determinato ambito della sottoscrizione o del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="cd268-103">This command lists all storage sync services within a given scope of subscription/resource group.</span></span>

## <span data-ttu-id="cd268-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cd268-104">SYNTAX</span></span>

### <span data-ttu-id="cd268-105">ParentStringParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cd268-105">ParentStringParameterSet (Default)</span></span>
```
Get-AzStorageSyncService [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cd268-106">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd268-106">StringParameterSet</span></span>
```
Get-AzStorageSyncService [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cd268-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="cd268-107">DESCRIPTION</span></span>
<span data-ttu-id="cd268-108">Questo comando elenca tutti i servizi di sincronizzazione di archiviazione in un determinato ambito della sottoscrizione o del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="cd268-108">This command lists all storage sync services within a given scope of subscription/resource group.</span></span> <span data-ttu-id="cd268-109">Può essere usato anche per elencare gli attributi di ogni servizio di sincronizzazione di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="cd268-109">It can be used to also list the attributes of each storage sync service.</span></span>

## <span data-ttu-id="cd268-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cd268-110">EXAMPLES</span></span>

### <span data-ttu-id="cd268-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="cd268-111">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncService -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="cd268-112">Questo comando elenca tutte le risorse del servizio di sincronizzazione di archiviazione all'interno di un determinato gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="cd268-112">This command lists all storage sync service resources within a given resource group.</span></span> <span data-ttu-id="cd268-113">Può essere usato anche per elencare gli attributi di ogni servizio di sincronizzazione di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="cd268-113">It can be used to also list the attributes of each storage sync service.</span></span> <span data-ttu-id="cd268-114">Specificare -StorageSyncServiceName per restituire un servizio specifico.</span><span class="sxs-lookup"><span data-stu-id="cd268-114">Specify -StorageSyncServiceName to return a specific one.</span></span>

## <span data-ttu-id="cd268-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cd268-115">PARAMETERS</span></span>

### <span data-ttu-id="cd268-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd268-116">-DefaultProfile</span></span>
<span data-ttu-id="cd268-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cd268-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd268-118">-Name</span><span class="sxs-lookup"><span data-stu-id="cd268-118">-Name</span></span>
<span data-ttu-id="cd268-119">Nome del servizio di sincronizzazione di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="cd268-119">Name of the storage sync service.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: StorageSyncServiceName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd268-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd268-120">-ResourceGroupName</span></span>
<span data-ttu-id="cd268-121">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="cd268-121">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ParentStringParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd268-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd268-122">CommonParameters</span></span>
<span data-ttu-id="cd268-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd268-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd268-124">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd268-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd268-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="cd268-125">INPUTS</span></span>

### <span data-ttu-id="cd268-126">System.String</span><span class="sxs-lookup"><span data-stu-id="cd268-126">System.String</span></span>

## <span data-ttu-id="cd268-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cd268-127">OUTPUTS</span></span>

### <span data-ttu-id="cd268-128">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="cd268-128">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="cd268-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="cd268-129">NOTES</span></span>

## <span data-ttu-id="cd268-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cd268-130">RELATED LINKS</span></span>
