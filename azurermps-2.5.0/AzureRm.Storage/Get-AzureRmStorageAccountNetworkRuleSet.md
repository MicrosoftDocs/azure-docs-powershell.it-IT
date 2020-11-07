---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/get-azurermstorageaccountnetworkruleset
schema: 2.0.0
ms.openlocfilehash: 8e3aa3bd313947712ef3831b83c75bb1349adb4f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866180"
---
# <span data-ttu-id="07c09-101">Get-AzureRmStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="07c09-101">Get-AzureRmStorageAccountNetworkRuleSet</span></span>

## <span data-ttu-id="07c09-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="07c09-102">SYNOPSIS</span></span>
<span data-ttu-id="07c09-103">Ottenere la proprietà NetWorkRule di un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="07c09-103">Get the NetWorkRule property of a Storage account</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07c09-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="07c09-104">SYNTAX</span></span>

```
Get-AzureRmStorageAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07c09-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="07c09-105">DESCRIPTION</span></span>
<span data-ttu-id="07c09-106">Il cmdlet **Get-AzureRmStorageAccountNetworkRuleSet** ottiene la proprietà NetworkRule di un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="07c09-106">The **Get-AzureRmStorageAccountNetworkRuleSet** cmdlet gets the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="07c09-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="07c09-107">EXAMPLES</span></span>

### <span data-ttu-id="07c09-108">Esempio 1: ottenere la proprietà NetworkRule di un account di archiviazione specificato</span><span class="sxs-lookup"><span data-stu-id="07c09-108">Example 1: Get NetworkRule property of a specified Storage account</span></span>
```
PS C:\> Get-AzureRmStorageAccountNetworkRuleSet  -ResourceGroupName "rg1" -AccountName "mystorageaccount"
```

<span data-ttu-id="07c09-109">Questo comando ottiene la proprietà NetworkRule di un account di archiviazione specificato</span><span class="sxs-lookup"><span data-stu-id="07c09-109">This command gets NetworkRule property of a specified Storage account</span></span>

## <span data-ttu-id="07c09-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="07c09-110">PARAMETERS</span></span>

### <span data-ttu-id="07c09-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07c09-111">-DefaultProfile</span></span>
<span data-ttu-id="07c09-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="07c09-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07c09-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="07c09-113">-Name</span></span>
<span data-ttu-id="07c09-114">Specifica il nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="07c09-114">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="07c09-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07c09-115">-ResourceGroupName</span></span>
<span data-ttu-id="07c09-116">Specifica il nome del gruppo di risorse che contiene l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="07c09-116">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="07c09-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07c09-117">CommonParameters</span></span>
<span data-ttu-id="07c09-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07c09-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07c09-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07c09-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07c09-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="07c09-120">INPUTS</span></span>

### <span data-ttu-id="07c09-121">System. String</span><span class="sxs-lookup"><span data-stu-id="07c09-121">System.String</span></span>

## <span data-ttu-id="07c09-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="07c09-122">OUTPUTS</span></span>

### <span data-ttu-id="07c09-123">Microsoft. Azure. Commands. Management. storage. Models. PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="07c09-123">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="07c09-124">Note</span><span class="sxs-lookup"><span data-stu-id="07c09-124">NOTES</span></span>

## <span data-ttu-id="07c09-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="07c09-125">RELATED LINKS</span></span>
