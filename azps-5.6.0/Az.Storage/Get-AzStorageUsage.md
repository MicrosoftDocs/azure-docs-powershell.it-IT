---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 11AAA319-DDBB-4156-9BE7-4DE8B80A904C
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstorageusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageUsage.md
ms.openlocfilehash: 9e12aa08bd37a5dfa467b2df03df42f5c58e4186
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994781"
---
# <span data-ttu-id="d496f-101">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="d496f-101">Get-AzStorageUsage</span></span>

## <span data-ttu-id="d496f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d496f-102">SYNOPSIS</span></span>
<span data-ttu-id="d496f-103">Ottiene l'uso delle risorse di archiviazione della sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="d496f-103">Gets the Storage resource usage of the current subscription.</span></span>

## <span data-ttu-id="d496f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d496f-104">SYNTAX</span></span>

```
Get-AzStorageUsage -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d496f-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d496f-105">DESCRIPTION</span></span>
<span data-ttu-id="d496f-106">Il cmdlet **Get-AzStorageUsage** ottiene l'utilizzo delle risorse per Archiviazione di Azure per la sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="d496f-106">The **Get-AzStorageUsage** cmdlet gets the resource usage for Azure Storage for the current subscription.</span></span>

## <span data-ttu-id="d496f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d496f-107">EXAMPLES</span></span>

### <span data-ttu-id="d496f-108">Esempio 1: Ottenere l'utilizzo delle risorse di archiviazione della posizione specificata</span><span class="sxs-lookup"><span data-stu-id="d496f-108">Example 1: Get the storage resources usage of specified location</span></span>
```
PS C:\>Get-AzStorageUsage -Location 'West US'

LocalizedName : Storage Accounts
Name          : StorageAccounts
Unit          : Count
CurrentValue  : 18
Limit         : 250
```

<span data-ttu-id="d496f-109">Questo comando recupera l'uso delle risorse di archiviazione della posizione specificata nella sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="d496f-109">This command gets the Storage resources usage of specified location under the current subscription.</span></span>

## <span data-ttu-id="d496f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d496f-110">PARAMETERS</span></span>

### <span data-ttu-id="d496f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d496f-111">-DefaultProfile</span></span>
<span data-ttu-id="d496f-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d496f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d496f-113">-Location</span><span class="sxs-lookup"><span data-stu-id="d496f-113">-Location</span></span>
<span data-ttu-id="d496f-114">Indicare di ottenere l'utilizzo delle risorse di archiviazione nella posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="d496f-114">Indicate to get Storage resources usage on the specified location.</span></span>
<span data-ttu-id="d496f-115">Se non è specificato, l'utilizzo delle risorse di archiviazione verrà visualizzato in tutte le posizioni della sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="d496f-115">If not specified, will get Storage resources usage on all locations under the subscription.</span></span>

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

### <span data-ttu-id="d496f-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d496f-116">CommonParameters</span></span>
<span data-ttu-id="d496f-117">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d496f-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d496f-118">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d496f-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d496f-119">INPUT</span><span class="sxs-lookup"><span data-stu-id="d496f-119">INPUTS</span></span>

### <span data-ttu-id="d496f-120">System.String</span><span class="sxs-lookup"><span data-stu-id="d496f-120">System.String</span></span>

## <span data-ttu-id="d496f-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d496f-121">OUTPUTS</span></span>

### <span data-ttu-id="d496f-122">Microsoft.Azure.Commands.Management.Storage.Models.PSUsage</span><span class="sxs-lookup"><span data-stu-id="d496f-122">Microsoft.Azure.Commands.Management.Storage.Models.PSUsage</span></span>

## <span data-ttu-id="d496f-123">NOTE</span><span class="sxs-lookup"><span data-stu-id="d496f-123">NOTES</span></span>

## <span data-ttu-id="d496f-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d496f-124">RELATED LINKS</span></span>

[<span data-ttu-id="d496f-125">Cmdlet di Gestione archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="d496f-125">Azure Storage Manager Cmdlets</span></span>](./Az.Storage.md)


