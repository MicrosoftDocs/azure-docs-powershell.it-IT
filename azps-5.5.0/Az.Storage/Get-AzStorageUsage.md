---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 11AAA319-DDBB-4156-9BE7-4DE8B80A904C
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageUsage.md
ms.openlocfilehash: 3d1fd5fb49b90a7d1a149cf83e8ee19c9eed5272
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183198"
---
# <span data-ttu-id="260e8-101">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="260e8-101">Get-AzStorageUsage</span></span>

## <span data-ttu-id="260e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="260e8-102">SYNOPSIS</span></span>
<span data-ttu-id="260e8-103">Ottiene l'uso delle risorse di archiviazione della sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="260e8-103">Gets the Storage resource usage of the current subscription.</span></span>

## <span data-ttu-id="260e8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="260e8-104">SYNTAX</span></span>

```
Get-AzStorageUsage -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="260e8-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="260e8-105">DESCRIPTION</span></span>
<span data-ttu-id="260e8-106">Il cmdlet **Get-AzStorageUsage** ottiene l'utilizzo delle risorse per Archiviazione di Azure per la sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="260e8-106">The **Get-AzStorageUsage** cmdlet gets the resource usage for Azure Storage for the current subscription.</span></span>

## <span data-ttu-id="260e8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="260e8-107">EXAMPLES</span></span>

### <span data-ttu-id="260e8-108">Esempio 1: Ottenere l'utilizzo delle risorse di archiviazione per la posizione specificata</span><span class="sxs-lookup"><span data-stu-id="260e8-108">Example 1: Get the storage resources usage of specified location</span></span>
```
PS C:\>Get-AzStorageUsage -Location 'West US'

LocalizedName : Storage Accounts
Name          : StorageAccounts
Unit          : Count
CurrentValue  : 18
Limit         : 250
```

<span data-ttu-id="260e8-109">Questo comando recupera l'uso delle risorse di archiviazione della posizione specificata nella sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="260e8-109">This command gets the Storage resources usage of specified location under the current subscription.</span></span>

## <span data-ttu-id="260e8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="260e8-110">PARAMETERS</span></span>

### <span data-ttu-id="260e8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="260e8-111">-DefaultProfile</span></span>
<span data-ttu-id="260e8-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="260e8-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="260e8-113">-Location</span><span class="sxs-lookup"><span data-stu-id="260e8-113">-Location</span></span>
<span data-ttu-id="260e8-114">Indicare di ottenere l'utilizzo delle risorse di archiviazione nella posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="260e8-114">Indicate to get Storage resources usage on the specified location.</span></span>
<span data-ttu-id="260e8-115">Se non è specificato, l'utilizzo delle risorse di archiviazione verrà visualizzato in tutte le posizioni della sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="260e8-115">If not specified, will get Storage resources usage on all locations under the subscription.</span></span>

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

### <span data-ttu-id="260e8-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="260e8-116">CommonParameters</span></span>
<span data-ttu-id="260e8-117">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="260e8-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="260e8-118">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="260e8-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="260e8-119">INPUT</span><span class="sxs-lookup"><span data-stu-id="260e8-119">INPUTS</span></span>

### <span data-ttu-id="260e8-120">System.String</span><span class="sxs-lookup"><span data-stu-id="260e8-120">System.String</span></span>

## <span data-ttu-id="260e8-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="260e8-121">OUTPUTS</span></span>

### <span data-ttu-id="260e8-122">Microsoft.Azure.Commands.Management.Storage.Models.PSUsage</span><span class="sxs-lookup"><span data-stu-id="260e8-122">Microsoft.Azure.Commands.Management.Storage.Models.PSUsage</span></span>

## <span data-ttu-id="260e8-123">NOTE</span><span class="sxs-lookup"><span data-stu-id="260e8-123">NOTES</span></span>

## <span data-ttu-id="260e8-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="260e8-124">RELATED LINKS</span></span>

[<span data-ttu-id="260e8-125">Cmdlet di Gestione archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="260e8-125">Azure Storage Manager Cmdlets</span></span>](./Az.Storage.md)


