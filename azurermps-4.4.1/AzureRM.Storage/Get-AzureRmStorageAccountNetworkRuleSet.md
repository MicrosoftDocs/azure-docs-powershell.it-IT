---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccountNetworkRuleSet.md
ms.openlocfilehash: 00447be14fe61b76a4dbb4f62e3393bb76c1ddb8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688491"
---
# <span data-ttu-id="6128f-101">Get-AzureRmStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="6128f-101">Get-AzureRmStorageAccountNetworkRuleSet</span></span>

## <span data-ttu-id="6128f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6128f-102">SYNOPSIS</span></span>
<span data-ttu-id="6128f-103">Ottenere la proprietà NetWorkRule di un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="6128f-103">Get the NetWorkRule property of a Storage Account</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6128f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6128f-104">SYNTAX</span></span>

```
Get-AzureRmStorageAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6128f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6128f-105">DESCRIPTION</span></span>
<span data-ttu-id="6128f-106">Il cmdlet **Get-AzureRmStorageAccountNetworkRuleSet** ottiene la proprietà NetworkRule di un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="6128f-106">The **Get-AzureRmStorageAccountNetworkRuleSet** cmdlet gets the NetworkRule property of a Storage Account</span></span>

## <span data-ttu-id="6128f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6128f-107">EXAMPLES</span></span>

### <span data-ttu-id="6128f-108">Esempio 1: ottenere la proprietà NetworkRule di un account di archiviazione specificato</span><span class="sxs-lookup"><span data-stu-id="6128f-108">Example 1: Get NetworkRule property of a specified storage account</span></span>
```
PS C:\> Get-AzureRmStorageAccountNetworkRuleSet  -ResourceGroupName "rg1" -AccountName "mystorageaccount"
```

<span data-ttu-id="6128f-109">Questo comando ottiene la proprietà NetworkRule di un account di archiviazione specificato</span><span class="sxs-lookup"><span data-stu-id="6128f-109">This command gets NetworkRule property of a specified storage account</span></span>

## <span data-ttu-id="6128f-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6128f-110">PARAMETERS</span></span>

### <span data-ttu-id="6128f-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="6128f-111">-Name</span></span>
<span data-ttu-id="6128f-112">Specifica il nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="6128f-112">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="6128f-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6128f-113">-ResourceGroupName</span></span>
<span data-ttu-id="6128f-114">Specifica il nome del gruppo di risorse che contiene l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="6128f-114">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="6128f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6128f-115">-DefaultProfile</span></span>
<span data-ttu-id="6128f-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6128f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6128f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6128f-117">CommonParameters</span></span>
<span data-ttu-id="6128f-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6128f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6128f-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6128f-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6128f-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6128f-120">INPUTS</span></span>

### <span data-ttu-id="6128f-121">System. String</span><span class="sxs-lookup"><span data-stu-id="6128f-121">System.String</span></span>

## <span data-ttu-id="6128f-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6128f-122">OUTPUTS</span></span>

### <span data-ttu-id="6128f-123">Microsoft. Azure. Commands. Management. storage. Models. PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="6128f-123">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="6128f-124">Note</span><span class="sxs-lookup"><span data-stu-id="6128f-124">NOTES</span></span>

## <span data-ttu-id="6128f-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6128f-125">RELATED LINKS</span></span>

