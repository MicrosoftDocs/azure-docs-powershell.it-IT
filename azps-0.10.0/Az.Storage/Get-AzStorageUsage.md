---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 11AAA319-DDBB-4156-9BE7-4DE8B80A904C
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageUsage.md
ms.openlocfilehash: edf78ad4022b29251d78e976ff7e5d66ae67bb69
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93862186"
---
# <span data-ttu-id="b47d6-101">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="b47d6-101">Get-AzStorageUsage</span></span>

## <span data-ttu-id="b47d6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b47d6-102">SYNOPSIS</span></span>
<span data-ttu-id="b47d6-103">Ottiene l'utilizzo della risorsa di archiviazione dell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="b47d6-103">Gets the Storage resource usage of the current subscription.</span></span>

## <span data-ttu-id="b47d6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b47d6-104">SYNTAX</span></span>

```
Get-AzStorageUsage [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b47d6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b47d6-105">DESCRIPTION</span></span>
<span data-ttu-id="b47d6-106">Il cmdlet **Get-AzStorageUsage** Ottiene l'utilizzo delle risorse per l'archiviazione di Azure per l'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="b47d6-106">The **Get-AzStorageUsage** cmdlet gets the resource usage for Azure Storage for the current subscription.</span></span>

## <span data-ttu-id="b47d6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b47d6-107">EXAMPLES</span></span>

### <span data-ttu-id="b47d6-108">Esempio 1: ottenere l'utilizzo delle risorse di archiviazione</span><span class="sxs-lookup"><span data-stu-id="b47d6-108">Example 1: Get the storage resources usage</span></span>
```
PS C:\>Get-AzStorageUsage
```

<span data-ttu-id="b47d6-109">Questo comando consente di ottenere l'utilizzo delle risorse di archiviazione dell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="b47d6-109">This command gets the Storage resources usage of the current subscription.</span></span>

## <span data-ttu-id="b47d6-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b47d6-110">PARAMETERS</span></span>

### <span data-ttu-id="b47d6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b47d6-111">-DefaultProfile</span></span>
<span data-ttu-id="b47d6-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b47d6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b47d6-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b47d6-113">CommonParameters</span></span>
<span data-ttu-id="b47d6-114">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b47d6-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b47d6-115">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b47d6-115">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b47d6-116">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b47d6-116">INPUTS</span></span>

### <span data-ttu-id="b47d6-117">Nessuno</span><span class="sxs-lookup"><span data-stu-id="b47d6-117">None</span></span>

## <span data-ttu-id="b47d6-118">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b47d6-118">OUTPUTS</span></span>

### <span data-ttu-id="b47d6-119">Microsoft. Azure. Commands. Management. storage. Models. PSUsage</span><span class="sxs-lookup"><span data-stu-id="b47d6-119">Microsoft.Azure.Commands.Management.Storage.Models.PSUsage</span></span>

## <span data-ttu-id="b47d6-120">Note</span><span class="sxs-lookup"><span data-stu-id="b47d6-120">NOTES</span></span>

## <span data-ttu-id="b47d6-121">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b47d6-121">RELATED LINKS</span></span>

[<span data-ttu-id="b47d6-122">Cmdlet di Azure Storage Manager</span><span class="sxs-lookup"><span data-stu-id="b47d6-122">Azure Storage Manager Cmdlets</span></span>](./Az.Storage.md)


