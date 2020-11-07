---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncService.md
ms.openlocfilehash: c724527b380e0004d30e0790024634bcc6ce550d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676459"
---
# <span data-ttu-id="1994d-101">Get-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="1994d-101">Get-AzStorageSyncService</span></span>

## <span data-ttu-id="1994d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1994d-102">SYNOPSIS</span></span>
<span data-ttu-id="1994d-103">Questo comando elenca tutti i servizi di sincronizzazione dello storage all'interno di un ambito specifico del gruppo sottoscrizione/risorsa.</span><span class="sxs-lookup"><span data-stu-id="1994d-103">This command lists all storage sync services within a given scope of subscription/resource group.</span></span>

## <span data-ttu-id="1994d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1994d-104">SYNTAX</span></span>

### <span data-ttu-id="1994d-105">ParentStringParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1994d-105">ParentStringParameterSet (Default)</span></span>
```
Get-AzStorageSyncService [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1994d-106">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="1994d-106">StringParameterSet</span></span>
```
Get-AzStorageSyncService [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1994d-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1994d-107">DESCRIPTION</span></span>
<span data-ttu-id="1994d-108">Questo comando elenca tutti i servizi di sincronizzazione dello storage all'interno di un ambito specifico del gruppo sottoscrizione/risorsa.</span><span class="sxs-lookup"><span data-stu-id="1994d-108">This command lists all storage sync services within a given scope of subscription/resource group.</span></span> <span data-ttu-id="1994d-109">Può essere usato anche per elencare gli attributi di ogni servizio di sincronizzazione dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="1994d-109">It can be used to also list the attributes of each storage sync service.</span></span>

## <span data-ttu-id="1994d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1994d-110">EXAMPLES</span></span>

### <span data-ttu-id="1994d-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1994d-111">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncService -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="1994d-112">Questo comando elenca tutte le risorse del servizio di sincronizzazione dello storage in un gruppo di risorse specifico.</span><span class="sxs-lookup"><span data-stu-id="1994d-112">This command lists all storage sync service resources within a given resource group.</span></span> <span data-ttu-id="1994d-113">Può essere usato anche per elencare gli attributi di ogni servizio di sincronizzazione dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="1994d-113">It can be used to also list the attributes of each storage sync service.</span></span> <span data-ttu-id="1994d-114">Specifica-StorageSyncServiceName per restituirne uno specifico.</span><span class="sxs-lookup"><span data-stu-id="1994d-114">Specify -StorageSyncServiceName to return a specific one.</span></span>

## <span data-ttu-id="1994d-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1994d-115">PARAMETERS</span></span>

### <span data-ttu-id="1994d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1994d-116">-DefaultProfile</span></span>
<span data-ttu-id="1994d-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1994d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1994d-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="1994d-118">-Name</span></span>
<span data-ttu-id="1994d-119">Nome del servizio di sincronizzazione dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="1994d-119">Name of the storage sync service.</span></span>

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

### <span data-ttu-id="1994d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1994d-120">-ResourceGroupName</span></span>
<span data-ttu-id="1994d-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1994d-121">Resource Group Name.</span></span>

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

### <span data-ttu-id="1994d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1994d-122">CommonParameters</span></span>
<span data-ttu-id="1994d-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1994d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1994d-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1994d-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1994d-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1994d-125">INPUTS</span></span>

### <span data-ttu-id="1994d-126">System. String</span><span class="sxs-lookup"><span data-stu-id="1994d-126">System.String</span></span>

## <span data-ttu-id="1994d-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1994d-127">OUTPUTS</span></span>

### <span data-ttu-id="1994d-128">Microsoft. Azure. Commands. StorageSync. Models. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="1994d-128">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="1994d-129">Note</span><span class="sxs-lookup"><span data-stu-id="1994d-129">NOTES</span></span>

## <span data-ttu-id="1994d-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1994d-130">RELATED LINKS</span></span>
