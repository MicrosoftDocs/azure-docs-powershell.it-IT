---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: 11AAA319-DDBB-4156-9BE7-4DE8B80A904C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/get-azurermstorageusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageUsage.md
ms.openlocfilehash: c63573da3c12eb54329d05f49615057d0595b77c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517316"
---
# <span data-ttu-id="e3a0d-101">Get-AzureRmStorageUsage</span><span class="sxs-lookup"><span data-stu-id="e3a0d-101">Get-AzureRmStorageUsage</span></span>

## <span data-ttu-id="e3a0d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e3a0d-102">SYNOPSIS</span></span>
<span data-ttu-id="e3a0d-103">Ottiene l'utilizzo della risorsa di archiviazione dell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="e3a0d-103">Gets the Storage resource usage of the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e3a0d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e3a0d-104">SYNTAX</span></span>

```
Get-AzureRmStorageUsage [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3a0d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e3a0d-105">DESCRIPTION</span></span>
<span data-ttu-id="e3a0d-106">Il cmdlet **Get-AzureRmStorageUsage** Ottiene l'utilizzo delle risorse per l'archiviazione di Azure per l'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="e3a0d-106">The **Get-AzureRmStorageUsage** cmdlet gets the resource usage for Azure Storage for the current subscription.</span></span>

## <span data-ttu-id="e3a0d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e3a0d-107">EXAMPLES</span></span>

### <span data-ttu-id="e3a0d-108">Esempio 1: ottenere l'utilizzo delle risorse di archiviazione</span><span class="sxs-lookup"><span data-stu-id="e3a0d-108">Example 1: Get the storage resources usage</span></span>
```
PS C:\>Get-AzureRmStorageUsage
```

<span data-ttu-id="e3a0d-109">Questo comando consente di ottenere l'utilizzo delle risorse di archiviazione dell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="e3a0d-109">This command gets the Storage resources usage of the current subscription.</span></span>
 

### <span data-ttu-id="e3a0d-110">Esempio 2: ottenere l'utilizzo delle risorse di archiviazione della posizione specificata</span><span class="sxs-lookup"><span data-stu-id="e3a0d-110">Example 2: Get the storage resources usage of specified location</span></span>
```
PS C:\>Get-AzureRmStorageUsage -Location 'West US'

LocalizedName : Storage Accounts
Name          : StorageAccounts
Unit          : Count
CurrentValue  : 18
Limit         : 250
```

<span data-ttu-id="e3a0d-111">Questo comando consente di ottenere l'utilizzo delle risorse di archiviazione della posizione specificata sotto l'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="e3a0d-111">This command gets the Storage resources usage of the specified location under the current subscription.</span></span>

## <span data-ttu-id="e3a0d-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e3a0d-112">PARAMETERS</span></span>

### <span data-ttu-id="e3a0d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3a0d-113">-DefaultProfile</span></span>
<span data-ttu-id="e3a0d-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e3a0d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3a0d-115">-Posizione</span><span class="sxs-lookup"><span data-stu-id="e3a0d-115">-Location</span></span>
<span data-ttu-id="e3a0d-116">Indicare per ottenere l'utilizzo delle risorse di archiviazione nella posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="e3a0d-116">Indicate to get Storage resources usage on the specified location.</span></span>
<span data-ttu-id="e3a0d-117">Se non specificato, otterrà l'utilizzo delle risorse di archiviazione in tutti i percorsi della sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="e3a0d-117">If not specified, will get Storage resources usage on all locations under the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3a0d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3a0d-118">CommonParameters</span></span>
<span data-ttu-id="e3a0d-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3a0d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3a0d-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3a0d-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3a0d-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e3a0d-121">INPUTS</span></span>

### <span data-ttu-id="e3a0d-122">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e3a0d-122">None</span></span>

## <span data-ttu-id="e3a0d-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e3a0d-123">OUTPUTS</span></span>

### <span data-ttu-id="e3a0d-124">Microsoft. Azure. Commands. Management. storage. Models. PSUsage</span><span class="sxs-lookup"><span data-stu-id="e3a0d-124">Microsoft.Azure.Commands.Management.Storage.Models.PSUsage</span></span>

## <span data-ttu-id="e3a0d-125">Note</span><span class="sxs-lookup"><span data-stu-id="e3a0d-125">NOTES</span></span>

## <span data-ttu-id="e3a0d-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e3a0d-126">RELATED LINKS</span></span>

[<span data-ttu-id="e3a0d-127">Cmdlet di Azure Storage Manager</span><span class="sxs-lookup"><span data-stu-id="e3a0d-127">Azure Storage Manager Cmdlets</span></span>](./AzureRM.Storage.md)


