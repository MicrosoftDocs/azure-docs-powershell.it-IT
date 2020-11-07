---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountNetworkRuleSet.md
ms.openlocfilehash: 5b269eef98072a7daaaf21aa0160167bb714c77a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93857838"
---
# <span data-ttu-id="d1674-101">Get-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="d1674-101">Get-AzStorageAccountNetworkRuleSet</span></span>

## <span data-ttu-id="d1674-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d1674-102">SYNOPSIS</span></span>
<span data-ttu-id="d1674-103">Ottenere la proprietà NetWorkRule di un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="d1674-103">Get the NetWorkRule property of a Storage account</span></span>

## <span data-ttu-id="d1674-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d1674-104">SYNTAX</span></span>

```
Get-AzStorageAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d1674-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d1674-105">DESCRIPTION</span></span>
<span data-ttu-id="d1674-106">Il cmdlet **Get-AzStorageAccountNetworkRuleSet** ottiene la proprietà NetworkRule di un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="d1674-106">The **Get-AzStorageAccountNetworkRuleSet** cmdlet gets the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="d1674-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d1674-107">EXAMPLES</span></span>

### <span data-ttu-id="d1674-108">Esempio 1: ottenere la proprietà NetworkRule di un account di archiviazione specificato</span><span class="sxs-lookup"><span data-stu-id="d1674-108">Example 1: Get NetworkRule property of a specified Storage account</span></span>
```
PS C:\> Get-AzStorageAccountNetworkRuleSet  -ResourceGroupName "rg1" -AccountName "mystorageaccount"
```

<span data-ttu-id="d1674-109">Questo comando ottiene la proprietà NetworkRule di un account di archiviazione specificato</span><span class="sxs-lookup"><span data-stu-id="d1674-109">This command gets NetworkRule property of a specified Storage account</span></span>

## <span data-ttu-id="d1674-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d1674-110">PARAMETERS</span></span>

### <span data-ttu-id="d1674-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1674-111">-DefaultProfile</span></span>
<span data-ttu-id="d1674-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d1674-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1674-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="d1674-113">-Name</span></span>
<span data-ttu-id="d1674-114">Specifica il nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="d1674-114">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="d1674-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1674-115">-ResourceGroupName</span></span>
<span data-ttu-id="d1674-116">Specifica il nome del gruppo di risorse che contiene l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="d1674-116">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="d1674-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1674-117">CommonParameters</span></span>
<span data-ttu-id="d1674-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1674-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1674-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1674-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1674-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d1674-120">INPUTS</span></span>

### <span data-ttu-id="d1674-121">System. String</span><span class="sxs-lookup"><span data-stu-id="d1674-121">System.String</span></span>

## <span data-ttu-id="d1674-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d1674-122">OUTPUTS</span></span>

### <span data-ttu-id="d1674-123">Microsoft. Azure. Commands. Management. storage. Models. PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="d1674-123">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="d1674-124">Note</span><span class="sxs-lookup"><span data-stu-id="d1674-124">NOTES</span></span>

## <span data-ttu-id="d1674-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d1674-125">RELATED LINKS</span></span>
