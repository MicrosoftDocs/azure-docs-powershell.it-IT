---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 6C7A7E1A-87A2-4F0D-9091-413C111F47F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreFirewallRule.md
ms.openlocfilehash: e583379f9541c056943081b804a84ecd7bee7bf5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189718"
---
# <span data-ttu-id="a5825-101">Remove-AzDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="a5825-101">Remove-AzDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="a5825-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a5825-102">SYNOPSIS</span></span>
<span data-ttu-id="a5825-103">Rimuove la regola del firewall specificata nello Store Data Lake specificato.</span><span class="sxs-lookup"><span data-stu-id="a5825-103">Removes the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="a5825-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a5825-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreFirewallRule [-Account] <String> [[-Name] <String>] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a5825-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a5825-105">DESCRIPTION</span></span>
<span data-ttu-id="a5825-106">Il cmdlet **Remove-AzDataLakeStoreFirewallRule** rimuove la regola del firewall specificata nello Store Data Lake.</span><span class="sxs-lookup"><span data-stu-id="a5825-106">The **Remove-AzDataLakeStoreFirewallRule** cmdlet removes the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="a5825-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a5825-107">EXAMPLES</span></span>

### <span data-ttu-id="a5825-108">Esempio 1: rimuovere una regola del firewall da un account</span><span class="sxs-lookup"><span data-stu-id="a5825-108">Example 1: Remove a firewall rule from an account</span></span>
```
PS C:\> Remove-AzDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule
```

<span data-ttu-id="a5825-109">Rimuove la regola del firewall "MyFirewallRule" dall'account "ContosoADL"</span><span class="sxs-lookup"><span data-stu-id="a5825-109">Removes firewall rule "MyFirewallRule" from account "ContosoADL"</span></span>

## <span data-ttu-id="a5825-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a5825-110">PARAMETERS</span></span>

### <span data-ttu-id="a5825-111">-Account</span><span class="sxs-lookup"><span data-stu-id="a5825-111">-Account</span></span>
<span data-ttu-id="a5825-112">L'account di data Lake Store per aggiornare la regola del firewall in</span><span class="sxs-lookup"><span data-stu-id="a5825-112">The Data Lake Store account to update the firewall rule in</span></span>

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

### <span data-ttu-id="a5825-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5825-113">-DefaultProfile</span></span>
<span data-ttu-id="a5825-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="a5825-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a5825-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="a5825-115">-Name</span></span>
<span data-ttu-id="a5825-116">Nome della regola del firewall da eliminare.</span><span class="sxs-lookup"><span data-stu-id="a5825-116">The name of the firewall rule to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5825-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a5825-117">-PassThru</span></span>
<span data-ttu-id="a5825-118">Indica che deve essere restituita una risposta booleana che indica il risultato dell'operazione di eliminazione.</span><span class="sxs-lookup"><span data-stu-id="a5825-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5825-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5825-119">-ResourceGroupName</span></span>
<span data-ttu-id="a5825-120">Specifica il nome del gruppo di risorse che contiene l'account per cui rimuovere la regola del firewall.</span><span class="sxs-lookup"><span data-stu-id="a5825-120">Specifies the name of the resource group that contains the account to remove the firewall rule from.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5825-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a5825-121">-Confirm</span></span>
<span data-ttu-id="a5825-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5825-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5825-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5825-123">-WhatIf</span></span>
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

### <span data-ttu-id="a5825-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5825-124">CommonParameters</span></span>
<span data-ttu-id="a5825-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5825-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5825-126">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5825-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5825-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a5825-127">INPUTS</span></span>

### <span data-ttu-id="a5825-128">System. String</span><span class="sxs-lookup"><span data-stu-id="a5825-128">System.String</span></span>

### <span data-ttu-id="a5825-129">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a5825-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a5825-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a5825-130">OUTPUTS</span></span>

### <span data-ttu-id="a5825-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a5825-131">System.Boolean</span></span>

## <span data-ttu-id="a5825-132">Note</span><span class="sxs-lookup"><span data-stu-id="a5825-132">NOTES</span></span>

## <span data-ttu-id="a5825-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a5825-133">RELATED LINKS</span></span>