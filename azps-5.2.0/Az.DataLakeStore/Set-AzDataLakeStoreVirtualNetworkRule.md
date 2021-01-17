---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: 1c649a63e8ba57a3d2e9f9af28e0ce4b12ca9a0d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98354436"
---
# <span data-ttu-id="0d927-101">Set-AzDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="0d927-101">Set-AzDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="0d927-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0d927-102">SYNOPSIS</span></span>
<span data-ttu-id="0d927-103">Modifica la regola di rete virtuale specificata nell'archivio dati specificato del lago.</span><span class="sxs-lookup"><span data-stu-id="0d927-103">Modifies the specified virtual network rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="0d927-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0d927-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreVirtualNetworkRule [-Account] <String> [-Name] <String> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d927-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0d927-105">DESCRIPTION</span></span>
<span data-ttu-id="0d927-106">Il cmdlet **set-AzDataLakeStoreVirtualNetworkRule** modifica la regola di rete virtuale specificata nello Store Data Lake specificato.</span><span class="sxs-lookup"><span data-stu-id="0d927-106">The **Set-AzDataLakeStoreVirtualNetworkRule** cmdlet modifies the specified virtual network rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="0d927-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0d927-107">EXAMPLES</span></span>

### <span data-ttu-id="0d927-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0d927-108">Example 1</span></span>
```powershell
PS C:\> Set-AzDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET" -SubnetId "updatedId"

ResourceGroupName                :
AccountName                      :
VirtualNetworkRuleName           : myVNET
VirtualNetworkSubnetId           : /subscriptions/<subscriptionId>/resourceGroups/<resourceGroup>/providers/Microsoft.Network/virtualNetworks/myVNET/subnets/updatedId
IgnoreMissingVnetServiceEndpoint :
State                            :
```

<span data-ttu-id="0d927-109">Aggiorna l'ID subnet della regola di rete virtuale "myVNET" nell'account "DLS" in "updatedId"</span><span class="sxs-lookup"><span data-stu-id="0d927-109">Updates the subnet id of virtual network rule "myVNET" in account "dls" to "updatedId"</span></span>

## <span data-ttu-id="0d927-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0d927-110">PARAMETERS</span></span>

### <span data-ttu-id="0d927-111">-Account</span><span class="sxs-lookup"><span data-stu-id="0d927-111">-Account</span></span>
<span data-ttu-id="0d927-112">L'account di data Lake Store per aggiornare la regola della rete virtuale in</span><span class="sxs-lookup"><span data-stu-id="0d927-112">The Data Lake Store account to update the virtual network rule in</span></span>

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

### <span data-ttu-id="0d927-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d927-113">-DefaultProfile</span></span>
<span data-ttu-id="0d927-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0d927-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d927-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="0d927-115">-Name</span></span>
<span data-ttu-id="0d927-116">Nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="0d927-116">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="0d927-117">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="0d927-117">-SubnetId</span></span>
<span data-ttu-id="0d927-118">Inizio dell'intervallo IP valido per la regola di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="0d927-118">The start of the valid ip range for the virtual network rule</span></span>

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

### <span data-ttu-id="0d927-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0d927-119">-Confirm</span></span>
<span data-ttu-id="0d927-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0d927-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d927-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d927-121">-WhatIf</span></span>
<span data-ttu-id="0d927-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0d927-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d927-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0d927-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d927-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d927-124">CommonParameters</span></span>
<span data-ttu-id="0d927-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d927-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d927-126">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d927-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d927-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0d927-127">INPUTS</span></span>

### <span data-ttu-id="0d927-128">System. String</span><span class="sxs-lookup"><span data-stu-id="0d927-128">System.String</span></span>

## <span data-ttu-id="0d927-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0d927-129">OUTPUTS</span></span>

### <span data-ttu-id="0d927-130">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="0d927-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="0d927-131">Note</span><span class="sxs-lookup"><span data-stu-id="0d927-131">NOTES</span></span>

## <span data-ttu-id="0d927-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0d927-132">RELATED LINKS</span></span>
