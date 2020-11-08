---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: 1c649a63e8ba57a3d2e9f9af28e0ce4b12ca9a0d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190260"
---
# <span data-ttu-id="b94fe-101">Set-AzDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="b94fe-101">Set-AzDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="b94fe-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b94fe-102">SYNOPSIS</span></span>
<span data-ttu-id="b94fe-103">Modifica la regola di rete virtuale specificata nell'archivio dati specificato del lago.</span><span class="sxs-lookup"><span data-stu-id="b94fe-103">Modifies the specified virtual network rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="b94fe-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b94fe-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreVirtualNetworkRule [-Account] <String> [-Name] <String> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b94fe-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b94fe-105">DESCRIPTION</span></span>
<span data-ttu-id="b94fe-106">Il cmdlet **set-AzDataLakeStoreVirtualNetworkRule** modifica la regola di rete virtuale specificata nello Store Data Lake specificato.</span><span class="sxs-lookup"><span data-stu-id="b94fe-106">The **Set-AzDataLakeStoreVirtualNetworkRule** cmdlet modifies the specified virtual network rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="b94fe-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b94fe-107">EXAMPLES</span></span>

### <span data-ttu-id="b94fe-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b94fe-108">Example 1</span></span>
```powershell
PS C:\> Set-AzDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET" -SubnetId "updatedId"

ResourceGroupName                :
AccountName                      :
VirtualNetworkRuleName           : myVNET
VirtualNetworkSubnetId           : /subscriptions/<subscriptionId>/resourceGroups/<resourceGroup>/providers/Microsoft.Network/virtualNetworks/myVNET/subnets/updatedId
IgnoreMissingVnetServiceEndpoint :
State                            :
```

<span data-ttu-id="b94fe-109">Aggiorna l'ID subnet della regola di rete virtuale "myVNET" nell'account "DLS" in "updatedId"</span><span class="sxs-lookup"><span data-stu-id="b94fe-109">Updates the subnet id of virtual network rule "myVNET" in account "dls" to "updatedId"</span></span>

## <span data-ttu-id="b94fe-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b94fe-110">PARAMETERS</span></span>

### <span data-ttu-id="b94fe-111">-Account</span><span class="sxs-lookup"><span data-stu-id="b94fe-111">-Account</span></span>
<span data-ttu-id="b94fe-112">L'account di data Lake Store per aggiornare la regola della rete virtuale in</span><span class="sxs-lookup"><span data-stu-id="b94fe-112">The Data Lake Store account to update the virtual network rule in</span></span>

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

### <span data-ttu-id="b94fe-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b94fe-113">-DefaultProfile</span></span>
<span data-ttu-id="b94fe-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b94fe-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b94fe-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="b94fe-115">-Name</span></span>
<span data-ttu-id="b94fe-116">Nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="b94fe-116">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="b94fe-117">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="b94fe-117">-SubnetId</span></span>
<span data-ttu-id="b94fe-118">Inizio dell'intervallo IP valido per la regola di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="b94fe-118">The start of the valid ip range for the virtual network rule</span></span>

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

### <span data-ttu-id="b94fe-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b94fe-119">-Confirm</span></span>
<span data-ttu-id="b94fe-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b94fe-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b94fe-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b94fe-121">-WhatIf</span></span>
<span data-ttu-id="b94fe-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b94fe-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b94fe-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b94fe-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b94fe-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b94fe-124">CommonParameters</span></span>
<span data-ttu-id="b94fe-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b94fe-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b94fe-126">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b94fe-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b94fe-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b94fe-127">INPUTS</span></span>

### <span data-ttu-id="b94fe-128">System. String</span><span class="sxs-lookup"><span data-stu-id="b94fe-128">System.String</span></span>

## <span data-ttu-id="b94fe-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b94fe-129">OUTPUTS</span></span>

### <span data-ttu-id="b94fe-130">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="b94fe-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="b94fe-131">Note</span><span class="sxs-lookup"><span data-stu-id="b94fe-131">NOTES</span></span>

## <span data-ttu-id="b94fe-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b94fe-132">RELATED LINKS</span></span>
