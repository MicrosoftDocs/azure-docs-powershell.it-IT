---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: 95e18d7e36122ed199b4a4c880b4fc918f1164f5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297829"
---
# <span data-ttu-id="ab502-101">Get-AzDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ab502-101">Get-AzDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="ab502-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ab502-102">SYNOPSIS</span></span>
<span data-ttu-id="ab502-103">Ottiene le regole di rete virtuale specificate nello Store Data Lake.</span><span class="sxs-lookup"><span data-stu-id="ab502-103">Gets the specified virtual network rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="ab502-104">Se non è specificata alcuna regola di rete virtuale, elenca tutte le regole di rete virtuale per l'account.</span><span class="sxs-lookup"><span data-stu-id="ab502-104">If no virtual network rule is specified, then lists all virtual network rules for the account.</span></span>

## <span data-ttu-id="ab502-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ab502-105">SYNTAX</span></span>

```
Get-AzDataLakeStoreVirtualNetworkRule [-Account] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab502-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ab502-106">DESCRIPTION</span></span>
<span data-ttu-id="ab502-107">Il cmdlet Get-AzDataLakeStoreVirtualNetworkRule ottiene le regole di rete virtuali specificate nello Store Data Lake.</span><span class="sxs-lookup"><span data-stu-id="ab502-107">The Get-AzDataLakeStoreVirtualNetworkRule cmdlet gets the specified virtual network rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="ab502-108">Se non è specificata alcuna regola di rete virtuale, elenca tutte le regole di rete virtuale per l'account.</span><span class="sxs-lookup"><span data-stu-id="ab502-108">If no virtual network rule is specified, then lists all virtual network rules for the account.</span></span>

## <span data-ttu-id="ab502-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ab502-109">EXAMPLES</span></span>

### <span data-ttu-id="ab502-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ab502-110">Example 1</span></span>
```powershell
PS C:\> Get-AzDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET"

ResourceGroupName                :
AccountName                      :
VirtualNetworkRuleName           : myVNET
VirtualNetworkSubnetId           : /subscriptions/<subscriptionId>/resourceGroups/<resourceGroup>/providers/Microsoft.Network/virtualNetworks/myVNET/subnets/testId
IgnoreMissingVnetServiceEndpoint :
State                            :
```

<span data-ttu-id="ab502-111">Restituisce la regola di rete virtuale denominata "myVNET" dall'account "DLS"</span><span class="sxs-lookup"><span data-stu-id="ab502-111">Returns the virtual network rule named "myVNET" from account "dls"</span></span>

## <span data-ttu-id="ab502-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ab502-112">PARAMETERS</span></span>

### <span data-ttu-id="ab502-113">-Account</span><span class="sxs-lookup"><span data-stu-id="ab502-113">-Account</span></span>
<span data-ttu-id="ab502-114">L'account di data Lake Store per ottenere la regola di rete virtuale da</span><span class="sxs-lookup"><span data-stu-id="ab502-114">The Data Lake Store account to get the virtual network rule from</span></span>

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

### <span data-ttu-id="ab502-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab502-115">-DefaultProfile</span></span>
<span data-ttu-id="ab502-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ab502-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab502-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="ab502-117">-Name</span></span>
<span data-ttu-id="ab502-118">Nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="ab502-118">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="ab502-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab502-119">CommonParameters</span></span>
<span data-ttu-id="ab502-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab502-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab502-121">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab502-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab502-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ab502-122">INPUTS</span></span>

### <span data-ttu-id="ab502-123">System. String</span><span class="sxs-lookup"><span data-stu-id="ab502-123">System.String</span></span>

## <span data-ttu-id="ab502-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ab502-124">OUTPUTS</span></span>

### <span data-ttu-id="ab502-125">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ab502-125">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="ab502-126">Note</span><span class="sxs-lookup"><span data-stu-id="ab502-126">NOTES</span></span>

## <span data-ttu-id="ab502-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ab502-127">RELATED LINKS</span></span>
