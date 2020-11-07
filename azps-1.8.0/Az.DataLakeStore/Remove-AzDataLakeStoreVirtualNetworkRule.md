---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: 7faa09d45082e6443ab389ebe3a355c9656bb8e2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836272"
---
# <span data-ttu-id="3203f-101">Remove-AzDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="3203f-101">Remove-AzDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="3203f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3203f-102">SYNOPSIS</span></span>
<span data-ttu-id="3203f-103">Rimuove la regola di rete virtuale specificata nello Store Data Lake.</span><span class="sxs-lookup"><span data-stu-id="3203f-103">Removes the specified virtual network rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="3203f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3203f-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreVirtualNetworkRule [-Account] <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3203f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3203f-105">DESCRIPTION</span></span>
<span data-ttu-id="3203f-106">Il cmdlet **Remove-AzDataLakeStoreVirtualNetworkRule** rimuove la regola di rete virtuale specificata nello Store Data Lake di dati specificato.</span><span class="sxs-lookup"><span data-stu-id="3203f-106">The **Remove-AzDataLakeStoreVirtualNetworkRule** cmdlet removes the specified virtual network rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="3203f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3203f-107">EXAMPLES</span></span>

### <span data-ttu-id="3203f-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3203f-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET"
```

<span data-ttu-id="3203f-109">Rimuove la regola di rete virtuale "myVNET" dall'account "DLS"</span><span class="sxs-lookup"><span data-stu-id="3203f-109">Removes virtual network rule "myVNET" from account "dls"</span></span>

## <span data-ttu-id="3203f-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3203f-110">PARAMETERS</span></span>

### <span data-ttu-id="3203f-111">-Account</span><span class="sxs-lookup"><span data-stu-id="3203f-111">-Account</span></span>
<span data-ttu-id="3203f-112">L'account di data Lake Store per aggiornare la regola della rete virtuale in</span><span class="sxs-lookup"><span data-stu-id="3203f-112">The Data Lake Store account to update the virtual network rule in</span></span>

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

### <span data-ttu-id="3203f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3203f-113">-DefaultProfile</span></span>
<span data-ttu-id="3203f-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3203f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3203f-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="3203f-115">-Name</span></span>
<span data-ttu-id="3203f-116">Nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="3203f-116">The name of the virtual network rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3203f-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3203f-117">-PassThru</span></span>
<span data-ttu-id="3203f-118">Indica che deve essere restituita una risposta booleana che indica il risultato dell'operazione di eliminazione.</span><span class="sxs-lookup"><span data-stu-id="3203f-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3203f-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3203f-119">-Confirm</span></span>
<span data-ttu-id="3203f-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3203f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3203f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3203f-121">-WhatIf</span></span>
<span data-ttu-id="3203f-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3203f-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3203f-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3203f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3203f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3203f-124">CommonParameters</span></span>
<span data-ttu-id="3203f-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3203f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3203f-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3203f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3203f-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3203f-127">INPUTS</span></span>

### <span data-ttu-id="3203f-128">System. String</span><span class="sxs-lookup"><span data-stu-id="3203f-128">System.String</span></span>

## <span data-ttu-id="3203f-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3203f-129">OUTPUTS</span></span>

### <span data-ttu-id="3203f-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3203f-130">System.Boolean</span></span>

## <span data-ttu-id="3203f-131">Note</span><span class="sxs-lookup"><span data-stu-id="3203f-131">NOTES</span></span>

## <span data-ttu-id="3203f-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3203f-132">RELATED LINKS</span></span>
