---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: 11AAA319-DDBB-4156-9BE7-4DE8B80A904C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/get-azurermstorageusage
schema: 2.0.0
ms.openlocfilehash: ae6524c46ed97563e7bf6c948f550a393d74f582
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866177"
---
# <span data-ttu-id="7711b-101">Get-AzureRmStorageUsage</span><span class="sxs-lookup"><span data-stu-id="7711b-101">Get-AzureRmStorageUsage</span></span>

## <span data-ttu-id="7711b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7711b-102">SYNOPSIS</span></span>
<span data-ttu-id="7711b-103">Ottiene l'utilizzo della risorsa di archiviazione dell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="7711b-103">Gets the Storage resource usage of the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7711b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7711b-104">SYNTAX</span></span>

```
Get-AzureRmStorageUsage [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7711b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7711b-105">DESCRIPTION</span></span>
<span data-ttu-id="7711b-106">Il cmdlet **Get-AzureRmStorageUsage** Ottiene l'utilizzo delle risorse per l'archiviazione di Azure per l'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="7711b-106">The **Get-AzureRmStorageUsage** cmdlet gets the resource usage for Azure Storage for the current subscription.</span></span>

## <span data-ttu-id="7711b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7711b-107">EXAMPLES</span></span>

### <span data-ttu-id="7711b-108">Esempio 1: ottenere l'utilizzo delle risorse di archiviazione</span><span class="sxs-lookup"><span data-stu-id="7711b-108">Example 1: Get the storage resources usage</span></span>
```
PS C:\>Get-AzureRmStorageUsage
```

<span data-ttu-id="7711b-109">Questo comando consente di ottenere l'utilizzo delle risorse di archiviazione dell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="7711b-109">This command gets the Storage resources usage of the current subscription.</span></span>

## <span data-ttu-id="7711b-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7711b-110">PARAMETERS</span></span>

### <span data-ttu-id="7711b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7711b-111">-DefaultProfile</span></span>
<span data-ttu-id="7711b-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7711b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7711b-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7711b-113">CommonParameters</span></span>
<span data-ttu-id="7711b-114">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7711b-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7711b-115">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7711b-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7711b-116">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7711b-116">INPUTS</span></span>

### <span data-ttu-id="7711b-117">Nessuno</span><span class="sxs-lookup"><span data-stu-id="7711b-117">None</span></span>

## <span data-ttu-id="7711b-118">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7711b-118">OUTPUTS</span></span>

### <span data-ttu-id="7711b-119">Microsoft. Azure. Commands. Management. storage. Models. PSUsage</span><span class="sxs-lookup"><span data-stu-id="7711b-119">Microsoft.Azure.Commands.Management.Storage.Models.PSUsage</span></span>

## <span data-ttu-id="7711b-120">Note</span><span class="sxs-lookup"><span data-stu-id="7711b-120">NOTES</span></span>

## <span data-ttu-id="7711b-121">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7711b-121">RELATED LINKS</span></span>

[<span data-ttu-id="7711b-122">Cmdlet di Azure Storage Manager</span><span class="sxs-lookup"><span data-stu-id="7711b-122">Azure Storage Manager Cmdlets</span></span>](./AzureRM.Storage.md)


