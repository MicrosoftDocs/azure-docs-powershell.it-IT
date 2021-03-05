---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/get-azdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: ec5ac8ab949b95fba3f82ea795dadcecfac360ee
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977134"
---
# <span data-ttu-id="87a67-101">Get-AzDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="87a67-101">Get-AzDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="87a67-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87a67-102">SYNOPSIS</span></span>
<span data-ttu-id="87a67-103">Ottiene le regole di rete virtuale specificate nel Data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="87a67-103">Gets the specified virtual network rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="87a67-104">Se non viene specificata alcuna regola di rete virtuale, vengono elencate tutte le regole di rete virtuale per l'account.</span><span class="sxs-lookup"><span data-stu-id="87a67-104">If no virtual network rule is specified, then lists all virtual network rules for the account.</span></span>

## <span data-ttu-id="87a67-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="87a67-105">SYNTAX</span></span>

```
Get-AzDataLakeStoreVirtualNetworkRule [-Account] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="87a67-106">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="87a67-106">DESCRIPTION</span></span>
<span data-ttu-id="87a67-107">Il Get-AzDataLakeStoreVirtualNetworkRule cmdlet recupera le regole di rete virtuale specificate nel Data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="87a67-107">The Get-AzDataLakeStoreVirtualNetworkRule cmdlet gets the specified virtual network rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="87a67-108">Se non viene specificata alcuna regola di rete virtuale, vengono elencate tutte le regole di rete virtuale per l'account.</span><span class="sxs-lookup"><span data-stu-id="87a67-108">If no virtual network rule is specified, then lists all virtual network rules for the account.</span></span>

## <span data-ttu-id="87a67-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="87a67-109">EXAMPLES</span></span>

### <span data-ttu-id="87a67-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="87a67-110">Example 1</span></span>
```powershell
PS C:\> Get-AzDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET"

ResourceGroupName                :
AccountName                      :
VirtualNetworkRuleName           : myVNET
VirtualNetworkSubnetId           : /subscriptions/<subscriptionId>/resourceGroups/<resourceGroup>/providers/Microsoft.Network/virtualNetworks/myVNET/subnets/testId
IgnoreMissingVnetServiceEndpoint :
State                            :
```

<span data-ttu-id="87a67-111">Restituisce la regola di rete virtuale denominata "myVNET" dall'account "dls"</span><span class="sxs-lookup"><span data-stu-id="87a67-111">Returns the virtual network rule named "myVNET" from account "dls"</span></span>

## <span data-ttu-id="87a67-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="87a67-112">PARAMETERS</span></span>

### <span data-ttu-id="87a67-113">-Account</span><span class="sxs-lookup"><span data-stu-id="87a67-113">-Account</span></span>
<span data-ttu-id="87a67-114">Account Data Lake Store da cui ottenere la regola di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="87a67-114">The Data Lake Store account to get the virtual network rule from</span></span>

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

### <span data-ttu-id="87a67-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87a67-115">-DefaultProfile</span></span>
<span data-ttu-id="87a67-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="87a67-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87a67-117">-Name</span><span class="sxs-lookup"><span data-stu-id="87a67-117">-Name</span></span>
<span data-ttu-id="87a67-118">Nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="87a67-118">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="87a67-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87a67-119">CommonParameters</span></span>
<span data-ttu-id="87a67-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87a67-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87a67-121">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87a67-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87a67-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="87a67-122">INPUTS</span></span>

### <span data-ttu-id="87a67-123">System.String</span><span class="sxs-lookup"><span data-stu-id="87a67-123">System.String</span></span>

## <span data-ttu-id="87a67-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="87a67-124">OUTPUTS</span></span>

### <span data-ttu-id="87a67-125">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="87a67-125">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="87a67-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="87a67-126">NOTES</span></span>

## <span data-ttu-id="87a67-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="87a67-127">RELATED LINKS</span></span>
