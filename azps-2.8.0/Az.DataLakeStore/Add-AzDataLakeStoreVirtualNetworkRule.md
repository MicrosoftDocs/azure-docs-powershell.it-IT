---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/add-azdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: 4fccc705951ba944afdf13bf75d581e7c76d593f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674824"
---
# <span data-ttu-id="96679-101">Add-AzDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="96679-101">Add-AzDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="96679-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="96679-102">SYNOPSIS</span></span>
<span data-ttu-id="96679-103">Aggiunge una regola di rete virtuale all'account di data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="96679-103">Adds a virtual network rule to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="96679-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="96679-104">SYNTAX</span></span>

```
Add-AzDataLakeStoreVirtualNetworkRule [-Account] <String> [-Name] <String> [-SubnetId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96679-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="96679-105">DESCRIPTION</span></span>
<span data-ttu-id="96679-106">Il cmdlet **Add-AzDataLakeStoreVirtualNetworkRule** aggiunge una regola di rete virtuale all'account di data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="96679-106">The **Add-AzDataLakeStoreVirtualNetworkRule** cmdlet adds a virtual network rule to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="96679-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="96679-107">EXAMPLES</span></span>

### <span data-ttu-id="96679-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="96679-108">Example 1</span></span>
```powershell
PS C:\> Add-AzDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET" -SubnetId "testId"

ResourceGroupName                :
AccountName                      :
VirtualNetworkRuleName           : myVNET
VirtualNetworkSubnetId           : /subscriptions/<subscriptionId>/resourceGroups/<resourceGroup>/providers/Microsoft.Network/virtualNetworks/myVNET/subnets/testId
IgnoreMissingVnetServiceEndpoint :
State                            :
```

<span data-ttu-id="96679-109">Verrà creata una nuova regola di rete virtuale denominata "myVNET" nell'account "DLS" con un ID subnet "testId"</span><span class="sxs-lookup"><span data-stu-id="96679-109">This creates a new virtual network rule called "myVNET" in account "dls" with a subnet id "testId"</span></span>

## <span data-ttu-id="96679-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="96679-110">PARAMETERS</span></span>

### <span data-ttu-id="96679-111">-Account</span><span class="sxs-lookup"><span data-stu-id="96679-111">-Account</span></span>
<span data-ttu-id="96679-112">L'account di data Lake Store per aggiungere la regola di rete virtuale a</span><span class="sxs-lookup"><span data-stu-id="96679-112">The Data Lake Store account to add the virtual network rule to</span></span>

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

### <span data-ttu-id="96679-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96679-113">-DefaultProfile</span></span>
<span data-ttu-id="96679-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="96679-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96679-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="96679-115">-Name</span></span>
<span data-ttu-id="96679-116">Nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="96679-116">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="96679-117">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="96679-117">-SubnetId</span></span>
<span data-ttu-id="96679-118">SubnetId della regola di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="96679-118">The subnetId of the virtual network rule</span></span>

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

### <span data-ttu-id="96679-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="96679-119">-Confirm</span></span>
<span data-ttu-id="96679-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="96679-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96679-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96679-121">-WhatIf</span></span>
<span data-ttu-id="96679-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="96679-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96679-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="96679-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96679-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96679-124">CommonParameters</span></span>
<span data-ttu-id="96679-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96679-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96679-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96679-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96679-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="96679-127">INPUTS</span></span>

### <span data-ttu-id="96679-128">System. String</span><span class="sxs-lookup"><span data-stu-id="96679-128">System.String</span></span>

## <span data-ttu-id="96679-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="96679-129">OUTPUTS</span></span>

### <span data-ttu-id="96679-130">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="96679-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="96679-131">Note</span><span class="sxs-lookup"><span data-stu-id="96679-131">NOTES</span></span>

## <span data-ttu-id="96679-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="96679-132">RELATED LINKS</span></span>