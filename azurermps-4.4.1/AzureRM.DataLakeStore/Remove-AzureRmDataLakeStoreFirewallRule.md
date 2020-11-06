---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 6C7A7E1A-87A2-4F0D-9091-413C111F47F0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreFirewallRule.md
ms.openlocfilehash: 6bbdfa981ac1d9e80c377bf2835cff73c99a7a94
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519590"
---
# <span data-ttu-id="098cf-101">Remove-AzureRmDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="098cf-101">Remove-AzureRmDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="098cf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="098cf-102">SYNOPSIS</span></span>
<span data-ttu-id="098cf-103">Rimuove la regola del firewall specificata nello Store Data Lake specificato.</span><span class="sxs-lookup"><span data-stu-id="098cf-103">Removes the specified firewall rule in the specified Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="098cf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="098cf-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeStoreFirewallRule [-Account] <String> [[-Name] <String>] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="098cf-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="098cf-105">DESCRIPTION</span></span>
<span data-ttu-id="098cf-106">Il cmdlet **Remove-AzureRmDataLakeStoreFirewallRule** rimuove la regola del firewall specificata nello Store Data Lake.</span><span class="sxs-lookup"><span data-stu-id="098cf-106">The **Remove-AzureRmDataLakeStoreFirewallRule** cmdlet removes the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="098cf-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="098cf-107">EXAMPLES</span></span>

### <span data-ttu-id="098cf-108">Esempio 1: rimuovere una regola del firewall da un account</span><span class="sxs-lookup"><span data-stu-id="098cf-108">Example 1: Remove a firewall rule from an account</span></span>
```
PS C:\> Remove-AzureRmDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule
```

<span data-ttu-id="098cf-109">Rimuove la regola del firewall "MyFirewallRule" dall'account "ContosoADL"</span><span class="sxs-lookup"><span data-stu-id="098cf-109">Removes firewall rule "MyFirewallRule" from account "ContosoADL"</span></span>

## <span data-ttu-id="098cf-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="098cf-110">PARAMETERS</span></span>

### <span data-ttu-id="098cf-111">-Account</span><span class="sxs-lookup"><span data-stu-id="098cf-111">-Account</span></span>
<span data-ttu-id="098cf-112">L'account di data Lake Store per aggiornare la regola del firewall in</span><span class="sxs-lookup"><span data-stu-id="098cf-112">The Data Lake Store account to update the firewall rule in</span></span>

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

### <span data-ttu-id="098cf-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="098cf-113">-Name</span></span>
<span data-ttu-id="098cf-114">Nome della regola del firewall da eliminare.</span><span class="sxs-lookup"><span data-stu-id="098cf-114">The name of the firewall rule to delete.</span></span>

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

### <span data-ttu-id="098cf-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="098cf-115">-PassThru</span></span>
<span data-ttu-id="098cf-116">Indica che deve essere restituita una risposta booleana che indica il risultato dell'operazione di eliminazione.</span><span class="sxs-lookup"><span data-stu-id="098cf-116">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="098cf-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="098cf-117">-ResourceGroupName</span></span>
<span data-ttu-id="098cf-118">Specifica il nome del gruppo di risorse che contiene l'account per cui rimuovere la regola del firewall.</span><span class="sxs-lookup"><span data-stu-id="098cf-118">Specifies the name of the resource group that contains the account to remove the firewall rule from.</span></span>

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

### <span data-ttu-id="098cf-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="098cf-119">-Confirm</span></span>
<span data-ttu-id="098cf-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="098cf-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="098cf-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="098cf-121">-WhatIf</span></span>
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

### <span data-ttu-id="098cf-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="098cf-122">-DefaultProfile</span></span>
<span data-ttu-id="098cf-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="098cf-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="098cf-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="098cf-124">CommonParameters</span></span>
<span data-ttu-id="098cf-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="098cf-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="098cf-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="098cf-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="098cf-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="098cf-127">INPUTS</span></span>

## <span data-ttu-id="098cf-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="098cf-128">OUTPUTS</span></span>

### <span data-ttu-id="098cf-129">bool</span><span class="sxs-lookup"><span data-stu-id="098cf-129">bool</span></span>
<span data-ttu-id="098cf-130">Se PassThru è specificato, restituisce vero al completamento corretto.</span><span class="sxs-lookup"><span data-stu-id="098cf-130">If PassThru is specified, returns true upon successful completion.</span></span>

## <span data-ttu-id="098cf-131">Note</span><span class="sxs-lookup"><span data-stu-id="098cf-131">NOTES</span></span>

## <span data-ttu-id="098cf-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="098cf-132">RELATED LINKS</span></span>

