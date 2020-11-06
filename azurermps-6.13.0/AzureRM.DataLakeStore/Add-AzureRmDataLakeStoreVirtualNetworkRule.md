---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/add-azurermdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Add-AzureRmDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Add-AzureRmDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: a25125b8aa76fa8d2be99f7f80b8fea2383bdf02
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518728"
---
# <span data-ttu-id="3830e-101">Add-AzureRmDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="3830e-101">Add-AzureRmDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="3830e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3830e-102">SYNOPSIS</span></span>
<span data-ttu-id="3830e-103">Aggiunge una regola di rete virtuale all'account di data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="3830e-103">Adds a virtual network rule to the specified Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3830e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3830e-104">SYNTAX</span></span>

```
Add-AzureRmDataLakeStoreVirtualNetworkRule [-Account] <String> [-Name] <String> [-SubnetId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3830e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3830e-105">DESCRIPTION</span></span>
<span data-ttu-id="3830e-106">Il cmdlet **Add-AzureRmDataLakeStoreVirtualNetworkRule** aggiunge una regola di rete virtuale all'account di data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="3830e-106">The **Add-AzureRmDataLakeStoreVirtualNetworkRule** cmdlet adds a virtual network rule to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="3830e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3830e-107">EXAMPLES</span></span>

### <span data-ttu-id="3830e-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3830e-108">Example 1</span></span>
```powershell
PS C:\> Add-AzureRmDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET" -SubnetId "testId"

ResourceGroupName                :
AccountName                      :
VirtualNetworkRuleName           : myVNET
VirtualNetworkSubnetId           : /subscriptions/<subscriptionId>/resourceGroups/<resourceGroup>/providers/Microsoft.Network/virtualNetworks/myVNET/subnets/testId
IgnoreMissingVnetServiceEndpoint :
State                            :
```

<span data-ttu-id="3830e-109">Verrà creata una nuova regola di rete virtuale denominata "myVNET" nell'account "DLS" con un ID subnet "testId"</span><span class="sxs-lookup"><span data-stu-id="3830e-109">This creates a new virtual network rule called "myVNET" in account "dls" with a subnet id "testId"</span></span>

## <span data-ttu-id="3830e-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3830e-110">PARAMETERS</span></span>

### <span data-ttu-id="3830e-111">-Account</span><span class="sxs-lookup"><span data-stu-id="3830e-111">-Account</span></span>
<span data-ttu-id="3830e-112">L'account di data Lake Store per aggiungere la regola di rete virtuale a</span><span class="sxs-lookup"><span data-stu-id="3830e-112">The Data Lake Store account to add the virtual network rule to</span></span>

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

### <span data-ttu-id="3830e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3830e-113">-DefaultProfile</span></span>
<span data-ttu-id="3830e-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3830e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3830e-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="3830e-115">-Name</span></span>
<span data-ttu-id="3830e-116">Nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="3830e-116">The name of the virtual network rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3830e-117">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="3830e-117">-SubnetId</span></span>
<span data-ttu-id="3830e-118">SubnetId della regola di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="3830e-118">The subnetId of the virtual network rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3830e-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3830e-119">-Confirm</span></span>
<span data-ttu-id="3830e-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3830e-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3830e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3830e-121">-WhatIf</span></span>
<span data-ttu-id="3830e-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3830e-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3830e-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3830e-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3830e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3830e-124">CommonParameters</span></span>
<span data-ttu-id="3830e-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3830e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3830e-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3830e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3830e-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3830e-127">INPUTS</span></span>

### <span data-ttu-id="3830e-128">System. String</span><span class="sxs-lookup"><span data-stu-id="3830e-128">System.String</span></span>

## <span data-ttu-id="3830e-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3830e-129">OUTPUTS</span></span>

### <span data-ttu-id="3830e-130">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="3830e-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="3830e-131">Note</span><span class="sxs-lookup"><span data-stu-id="3830e-131">NOTES</span></span>

## <span data-ttu-id="3830e-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3830e-132">RELATED LINKS</span></span>
