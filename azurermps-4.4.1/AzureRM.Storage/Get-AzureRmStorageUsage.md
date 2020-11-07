---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: 11AAA319-DDBB-4156-9BE7-4DE8B80A904C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Get-AzureRmStorageUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Get-AzureRmStorageUsage.md
ms.openlocfilehash: 1ef273329634e080c4117b9ddd0d1eaf8d91bb0e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688485"
---
# <span data-ttu-id="24b0b-101">Get-AzureRmStorageUsage</span><span class="sxs-lookup"><span data-stu-id="24b0b-101">Get-AzureRmStorageUsage</span></span>

## <span data-ttu-id="24b0b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="24b0b-102">SYNOPSIS</span></span>
<span data-ttu-id="24b0b-103">Ottiene l'utilizzo della risorsa di archiviazione dell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="24b0b-103">Gets the Storage resource usage of the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24b0b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="24b0b-104">SYNTAX</span></span>

```
Get-AzureRmStorageUsage [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24b0b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="24b0b-105">DESCRIPTION</span></span>
<span data-ttu-id="24b0b-106">Il cmdlet **Get-AzureRmStorageUsage** Ottiene l'utilizzo delle risorse per l'archiviazione di Azure per l'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="24b0b-106">The **Get-AzureRmStorageUsage** cmdlet gets the resource usage for Azure Storage for the current subscription.</span></span>

## <span data-ttu-id="24b0b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="24b0b-107">EXAMPLES</span></span>

### <span data-ttu-id="24b0b-108">Esempio 1: ottenere l'utilizzo delle risorse di archiviazione</span><span class="sxs-lookup"><span data-stu-id="24b0b-108">Example 1: Get the storage resources usage</span></span>
```
PS C:\>Get-AzureRmStorageUsage
```

<span data-ttu-id="24b0b-109">Questo comando consente di ottenere l'utilizzo delle risorse di archiviazione dell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="24b0b-109">This command gets the Storage resources usage of the current subscription.</span></span>

## <span data-ttu-id="24b0b-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="24b0b-110">PARAMETERS</span></span>

### <span data-ttu-id="24b0b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24b0b-111">-DefaultProfile</span></span>
<span data-ttu-id="24b0b-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="24b0b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24b0b-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24b0b-113">CommonParameters</span></span>
<span data-ttu-id="24b0b-114">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24b0b-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24b0b-115">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24b0b-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24b0b-116">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="24b0b-116">INPUTS</span></span>

## <span data-ttu-id="24b0b-117">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="24b0b-117">OUTPUTS</span></span>

## <span data-ttu-id="24b0b-118">Note</span><span class="sxs-lookup"><span data-stu-id="24b0b-118">NOTES</span></span>

## <span data-ttu-id="24b0b-119">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="24b0b-119">RELATED LINKS</span></span>

[<span data-ttu-id="24b0b-120">Cmdlet di Azure Storage Manager</span><span class="sxs-lookup"><span data-stu-id="24b0b-120">Azure Storage Manager Cmdlets</span></span>](./AzureRM.Storage.md)


