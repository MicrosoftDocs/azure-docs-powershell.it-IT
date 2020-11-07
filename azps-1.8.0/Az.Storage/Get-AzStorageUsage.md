---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 11AAA319-DDBB-4156-9BE7-4DE8B80A904C
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageUsage.md
ms.openlocfilehash: 31729843425f2360f1716e2b0faffc72715b9a81
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676597"
---
# <span data-ttu-id="e6a74-101">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="e6a74-101">Get-AzStorageUsage</span></span>

## <span data-ttu-id="e6a74-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e6a74-102">SYNOPSIS</span></span>
<span data-ttu-id="e6a74-103">Ottiene l'utilizzo della risorsa di archiviazione dell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="e6a74-103">Gets the Storage resource usage of the current subscription.</span></span>

## <span data-ttu-id="e6a74-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e6a74-104">SYNTAX</span></span>

```
Get-AzStorageUsage -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e6a74-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e6a74-105">DESCRIPTION</span></span>
<span data-ttu-id="e6a74-106">Il cmdlet **Get-AzStorageUsage** Ottiene l'utilizzo delle risorse per l'archiviazione di Azure per l'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="e6a74-106">The **Get-AzStorageUsage** cmdlet gets the resource usage for Azure Storage for the current subscription.</span></span>

## <span data-ttu-id="e6a74-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e6a74-107">EXAMPLES</span></span>

### <span data-ttu-id="e6a74-108">Esempio 1: ottenere l'utilizzo delle risorse di archiviazione della posizione specificata</span><span class="sxs-lookup"><span data-stu-id="e6a74-108">Example 1: Get the storage resources usage of specified location</span></span>
```
PS C:\>Get-AzStorageUsage -Location 'West US'

LocalizedName : Storage Accounts
Name          : StorageAccounts
Unit          : Count
CurrentValue  : 18
Limit         : 250
```

<span data-ttu-id="e6a74-109">Questo comando consente di ottenere l'utilizzo delle risorse di archiviazione della posizione specificata sotto l'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="e6a74-109">This command gets the Storage resources usage of the specified location under the current subscription.</span></span>

## <span data-ttu-id="e6a74-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e6a74-110">PARAMETERS</span></span>

### <span data-ttu-id="e6a74-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6a74-111">-DefaultProfile</span></span>
<span data-ttu-id="e6a74-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e6a74-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6a74-113">-Posizione</span><span class="sxs-lookup"><span data-stu-id="e6a74-113">-Location</span></span>
<span data-ttu-id="e6a74-114">Indicare per ottenere l'utilizzo delle risorse di archiviazione nella posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="e6a74-114">Indicate to get Storage resources usage on the specified location.</span></span>
<span data-ttu-id="e6a74-115">Se non specificato, otterrà l'utilizzo delle risorse di archiviazione in tutti i percorsi della sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="e6a74-115">If not specified, will get Storage resources usage on all locations under the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6a74-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6a74-116">CommonParameters</span></span>
<span data-ttu-id="e6a74-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6a74-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6a74-118">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6a74-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6a74-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e6a74-119">INPUTS</span></span>

### <span data-ttu-id="e6a74-120">System. String</span><span class="sxs-lookup"><span data-stu-id="e6a74-120">System.String</span></span>

## <span data-ttu-id="e6a74-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e6a74-121">OUTPUTS</span></span>

### <span data-ttu-id="e6a74-122">Microsoft. Azure. Commands. Management. storage. Models. PSUsage</span><span class="sxs-lookup"><span data-stu-id="e6a74-122">Microsoft.Azure.Commands.Management.Storage.Models.PSUsage</span></span>

## <span data-ttu-id="e6a74-123">Note</span><span class="sxs-lookup"><span data-stu-id="e6a74-123">NOTES</span></span>

## <span data-ttu-id="e6a74-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e6a74-124">RELATED LINKS</span></span>

[<span data-ttu-id="e6a74-125">Cmdlet di Azure Storage Manager</span><span class="sxs-lookup"><span data-stu-id="e6a74-125">Azure Storage Manager Cmdlets</span></span>](./Az.Storage.md)


