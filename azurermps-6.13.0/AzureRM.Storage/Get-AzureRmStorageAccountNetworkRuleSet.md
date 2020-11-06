---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/get-azurermstorageaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccountNetworkRuleSet.md
ms.openlocfilehash: 0a316ee8e4d1d7c8d58e2444aa6cdfadbc5e0367
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514736"
---
# <span data-ttu-id="e5700-101">Get-AzureRmStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="e5700-101">Get-AzureRmStorageAccountNetworkRuleSet</span></span>

## <span data-ttu-id="e5700-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e5700-102">SYNOPSIS</span></span>
<span data-ttu-id="e5700-103">Ottenere la proprietà NetWorkRule di un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="e5700-103">Get the NetWorkRule property of a Storage account</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5700-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e5700-104">SYNTAX</span></span>

```
Get-AzureRmStorageAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5700-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e5700-105">DESCRIPTION</span></span>
<span data-ttu-id="e5700-106">Il cmdlet **Get-AzureRmStorageAccountNetworkRuleSet** ottiene la proprietà NetworkRule di un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="e5700-106">The **Get-AzureRmStorageAccountNetworkRuleSet** cmdlet gets the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="e5700-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e5700-107">EXAMPLES</span></span>

### <span data-ttu-id="e5700-108">Esempio 1: ottenere la proprietà NetworkRule di un account di archiviazione specificato</span><span class="sxs-lookup"><span data-stu-id="e5700-108">Example 1: Get NetworkRule property of a specified Storage account</span></span>
```
PS C:\> Get-AzureRmStorageAccountNetworkRuleSet  -ResourceGroupName "rg1" -AccountName "mystorageaccount"
```

<span data-ttu-id="e5700-109">Questo comando ottiene la proprietà NetworkRule di un account di archiviazione specificato</span><span class="sxs-lookup"><span data-stu-id="e5700-109">This command gets NetworkRule property of a specified Storage account</span></span>

## <span data-ttu-id="e5700-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e5700-110">PARAMETERS</span></span>

### <span data-ttu-id="e5700-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5700-111">-DefaultProfile</span></span>
<span data-ttu-id="e5700-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e5700-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5700-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="e5700-113">-Name</span></span>
<span data-ttu-id="e5700-114">Specifica il nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="e5700-114">Specifies the name of the Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5700-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5700-115">-ResourceGroupName</span></span>
<span data-ttu-id="e5700-116">Specifica il nome del gruppo di risorse che contiene l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="e5700-116">Specifies the name of the resource group contains the Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5700-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5700-117">CommonParameters</span></span>
<span data-ttu-id="e5700-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5700-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5700-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5700-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5700-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e5700-120">INPUTS</span></span>

### <span data-ttu-id="e5700-121">System. String</span><span class="sxs-lookup"><span data-stu-id="e5700-121">System.String</span></span>

## <span data-ttu-id="e5700-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e5700-122">OUTPUTS</span></span>

### <span data-ttu-id="e5700-123">Microsoft. Azure. Commands. Management. storage. Models. PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="e5700-123">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="e5700-124">Note</span><span class="sxs-lookup"><span data-stu-id="e5700-124">NOTES</span></span>

## <span data-ttu-id="e5700-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e5700-125">RELATED LINKS</span></span>
