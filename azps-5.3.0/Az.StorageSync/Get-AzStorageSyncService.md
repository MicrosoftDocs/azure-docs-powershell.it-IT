---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncService.md
ms.openlocfilehash: ec446a92c96bd92d7a4af5610f00ff76dcd50b50
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98474618"
---
# <span data-ttu-id="90211-101">Get-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="90211-101">Get-AzStorageSyncService</span></span>

## <span data-ttu-id="90211-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="90211-102">SYNOPSIS</span></span>
<span data-ttu-id="90211-103">Questo comando elenca tutti i servizi di sincronizzazione dello storage all'interno di un ambito specifico del gruppo sottoscrizione/risorsa.</span><span class="sxs-lookup"><span data-stu-id="90211-103">This command lists all storage sync services within a given scope of subscription/resource group.</span></span>

## <span data-ttu-id="90211-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="90211-104">SYNTAX</span></span>

### <span data-ttu-id="90211-105">ParentStringParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="90211-105">ParentStringParameterSet (Default)</span></span>
```
Get-AzStorageSyncService [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="90211-106">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="90211-106">StringParameterSet</span></span>
```
Get-AzStorageSyncService [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="90211-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="90211-107">DESCRIPTION</span></span>
<span data-ttu-id="90211-108">Questo comando elenca tutti i servizi di sincronizzazione dello storage all'interno di un ambito specifico del gruppo sottoscrizione/risorsa.</span><span class="sxs-lookup"><span data-stu-id="90211-108">This command lists all storage sync services within a given scope of subscription/resource group.</span></span> <span data-ttu-id="90211-109">Può essere usato anche per elencare gli attributi di ogni servizio di sincronizzazione dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="90211-109">It can be used to also list the attributes of each storage sync service.</span></span>

## <span data-ttu-id="90211-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="90211-110">EXAMPLES</span></span>

### <span data-ttu-id="90211-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="90211-111">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncService -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="90211-112">Questo comando elenca tutte le risorse del servizio di sincronizzazione dello storage in un gruppo di risorse specifico.</span><span class="sxs-lookup"><span data-stu-id="90211-112">This command lists all storage sync service resources within a given resource group.</span></span> <span data-ttu-id="90211-113">Può essere usato anche per elencare gli attributi di ogni servizio di sincronizzazione dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="90211-113">It can be used to also list the attributes of each storage sync service.</span></span> <span data-ttu-id="90211-114">Specifica-StorageSyncServiceName per restituirne uno specifico.</span><span class="sxs-lookup"><span data-stu-id="90211-114">Specify -StorageSyncServiceName to return a specific one.</span></span>

## <span data-ttu-id="90211-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="90211-115">PARAMETERS</span></span>

### <span data-ttu-id="90211-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90211-116">-DefaultProfile</span></span>
<span data-ttu-id="90211-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="90211-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90211-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="90211-118">-Name</span></span>
<span data-ttu-id="90211-119">Nome del servizio di sincronizzazione dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="90211-119">Name of the storage sync service.</span></span>

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

### <span data-ttu-id="90211-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90211-120">-ResourceGroupName</span></span>
<span data-ttu-id="90211-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="90211-121">Resource Group Name.</span></span>

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

### <span data-ttu-id="90211-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90211-122">CommonParameters</span></span>
<span data-ttu-id="90211-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90211-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90211-124">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90211-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90211-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="90211-125">INPUTS</span></span>

### <span data-ttu-id="90211-126">System. String</span><span class="sxs-lookup"><span data-stu-id="90211-126">System.String</span></span>

## <span data-ttu-id="90211-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="90211-127">OUTPUTS</span></span>

### <span data-ttu-id="90211-128">Microsoft. Azure. Commands. StorageSync. Models. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="90211-128">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="90211-129">Note</span><span class="sxs-lookup"><span data-stu-id="90211-129">NOTES</span></span>

## <span data-ttu-id="90211-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="90211-130">RELATED LINKS</span></span>
