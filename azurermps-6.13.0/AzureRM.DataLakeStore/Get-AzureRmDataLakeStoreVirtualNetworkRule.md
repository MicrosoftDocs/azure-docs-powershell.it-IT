---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: 1b404a42c3d40138408d7fb6f2c13a8af91c45c1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511723"
---
# <span data-ttu-id="b673e-101">Get-AzureRmDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="b673e-101">Get-AzureRmDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="b673e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b673e-102">SYNOPSIS</span></span>
<span data-ttu-id="b673e-103">Ottiene le regole di rete virtuale specificate nello Store Data Lake.</span><span class="sxs-lookup"><span data-stu-id="b673e-103">Gets the specified virtual network rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="b673e-104">Se non è specificata alcuna regola di rete virtuale, elenca tutte le regole di rete virtuale per l'account.</span><span class="sxs-lookup"><span data-stu-id="b673e-104">If no virtual network rule is specified, then lists all virtual network rules for the account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b673e-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b673e-105">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreVirtualNetworkRule [-Account] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b673e-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b673e-106">DESCRIPTION</span></span>
<span data-ttu-id="b673e-107">Il cmdlet Get-AzureRmDataLakeStoreVirtualNetworkRule ottiene le regole di rete virtuali specificate nello Store Data Lake.</span><span class="sxs-lookup"><span data-stu-id="b673e-107">The Get-AzureRmDataLakeStoreVirtualNetworkRule cmdlet gets the specified virtual network rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="b673e-108">Se non è specificata alcuna regola di rete virtuale, elenca tutte le regole di rete virtuale per l'account.</span><span class="sxs-lookup"><span data-stu-id="b673e-108">If no virtual network rule is specified, then lists all virtual network rules for the account.</span></span>

## <span data-ttu-id="b673e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b673e-109">EXAMPLES</span></span>

### <span data-ttu-id="b673e-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b673e-110">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET"

ResourceGroupName                :
AccountName                      :
VirtualNetworkRuleName           : myVNET
VirtualNetworkSubnetId           : /subscriptions/<subscriptionId>/resourceGroups/<resourceGroup>/providers/Microsoft.Network/virtualNetworks/myVNET/subnets/testId
IgnoreMissingVnetServiceEndpoint :
State                            :
```

<span data-ttu-id="b673e-111">Restituisce la regola di rete virtuale denominata "myVNET" dall'account "DLS"</span><span class="sxs-lookup"><span data-stu-id="b673e-111">Returns the virtual network rule named "myVNET" from account "dls"</span></span>

## <span data-ttu-id="b673e-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b673e-112">PARAMETERS</span></span>

### <span data-ttu-id="b673e-113">-Account</span><span class="sxs-lookup"><span data-stu-id="b673e-113">-Account</span></span>
<span data-ttu-id="b673e-114">L'account di data Lake Store per ottenere la regola di rete virtuale da</span><span class="sxs-lookup"><span data-stu-id="b673e-114">The Data Lake Store account to get the virtual network rule from</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b673e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b673e-115">-DefaultProfile</span></span>
<span data-ttu-id="b673e-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b673e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b673e-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="b673e-117">-Name</span></span>
<span data-ttu-id="b673e-118">Nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="b673e-118">The name of the virtual network rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b673e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b673e-119">CommonParameters</span></span>
<span data-ttu-id="b673e-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b673e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b673e-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b673e-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b673e-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b673e-122">INPUTS</span></span>

### <span data-ttu-id="b673e-123">System. String</span><span class="sxs-lookup"><span data-stu-id="b673e-123">System.String</span></span>

## <span data-ttu-id="b673e-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b673e-124">OUTPUTS</span></span>

### <span data-ttu-id="b673e-125">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="b673e-125">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="b673e-126">Note</span><span class="sxs-lookup"><span data-stu-id="b673e-126">NOTES</span></span>

## <span data-ttu-id="b673e-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b673e-127">RELATED LINKS</span></span>
