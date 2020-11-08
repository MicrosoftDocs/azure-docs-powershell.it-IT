---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: 95e18d7e36122ed199b4a4c880b4fc918f1164f5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189083"
---
# <span data-ttu-id="a1d21-101">Get-AzDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="a1d21-101">Get-AzDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="a1d21-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a1d21-102">SYNOPSIS</span></span>
<span data-ttu-id="a1d21-103">Ottiene le regole di rete virtuale specificate nello Store Data Lake.</span><span class="sxs-lookup"><span data-stu-id="a1d21-103">Gets the specified virtual network rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="a1d21-104">Se non è specificata alcuna regola di rete virtuale, elenca tutte le regole di rete virtuale per l'account.</span><span class="sxs-lookup"><span data-stu-id="a1d21-104">If no virtual network rule is specified, then lists all virtual network rules for the account.</span></span>

## <span data-ttu-id="a1d21-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a1d21-105">SYNTAX</span></span>

```
Get-AzDataLakeStoreVirtualNetworkRule [-Account] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1d21-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a1d21-106">DESCRIPTION</span></span>
<span data-ttu-id="a1d21-107">Il cmdlet Get-AzDataLakeStoreVirtualNetworkRule ottiene le regole di rete virtuali specificate nello Store Data Lake.</span><span class="sxs-lookup"><span data-stu-id="a1d21-107">The Get-AzDataLakeStoreVirtualNetworkRule cmdlet gets the specified virtual network rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="a1d21-108">Se non è specificata alcuna regola di rete virtuale, elenca tutte le regole di rete virtuale per l'account.</span><span class="sxs-lookup"><span data-stu-id="a1d21-108">If no virtual network rule is specified, then lists all virtual network rules for the account.</span></span>

## <span data-ttu-id="a1d21-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a1d21-109">EXAMPLES</span></span>

### <span data-ttu-id="a1d21-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a1d21-110">Example 1</span></span>
```powershell
PS C:\> Get-AzDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET"

ResourceGroupName                :
AccountName                      :
VirtualNetworkRuleName           : myVNET
VirtualNetworkSubnetId           : /subscriptions/<subscriptionId>/resourceGroups/<resourceGroup>/providers/Microsoft.Network/virtualNetworks/myVNET/subnets/testId
IgnoreMissingVnetServiceEndpoint :
State                            :
```

<span data-ttu-id="a1d21-111">Restituisce la regola di rete virtuale denominata "myVNET" dall'account "DLS"</span><span class="sxs-lookup"><span data-stu-id="a1d21-111">Returns the virtual network rule named "myVNET" from account "dls"</span></span>

## <span data-ttu-id="a1d21-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a1d21-112">PARAMETERS</span></span>

### <span data-ttu-id="a1d21-113">-Account</span><span class="sxs-lookup"><span data-stu-id="a1d21-113">-Account</span></span>
<span data-ttu-id="a1d21-114">L'account di data Lake Store per ottenere la regola di rete virtuale da</span><span class="sxs-lookup"><span data-stu-id="a1d21-114">The Data Lake Store account to get the virtual network rule from</span></span>

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

### <span data-ttu-id="a1d21-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1d21-115">-DefaultProfile</span></span>
<span data-ttu-id="a1d21-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a1d21-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1d21-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="a1d21-117">-Name</span></span>
<span data-ttu-id="a1d21-118">Nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="a1d21-118">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="a1d21-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1d21-119">CommonParameters</span></span>
<span data-ttu-id="a1d21-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1d21-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1d21-121">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1d21-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1d21-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a1d21-122">INPUTS</span></span>

### <span data-ttu-id="a1d21-123">System. String</span><span class="sxs-lookup"><span data-stu-id="a1d21-123">System.String</span></span>

## <span data-ttu-id="a1d21-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a1d21-124">OUTPUTS</span></span>

### <span data-ttu-id="a1d21-125">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="a1d21-125">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="a1d21-126">Note</span><span class="sxs-lookup"><span data-stu-id="a1d21-126">NOTES</span></span>

## <span data-ttu-id="a1d21-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a1d21-127">RELATED LINKS</span></span>
