---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: C6FD4734-720C-4C8C-9B58-EDB331DD6415
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/add-azdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreFirewallRule.md
ms.openlocfilehash: 9fa890ee6102f4751b62325b3cc3669d337cb6c4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674833"
---
# <span data-ttu-id="f7446-101">Add-AzDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f7446-101">Add-AzDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="f7446-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f7446-102">SYNOPSIS</span></span>
<span data-ttu-id="f7446-103">Aggiunge una regola del firewall all'account di data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="f7446-103">Adds a firewall rule to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="f7446-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f7446-104">SYNTAX</span></span>

```
Add-AzDataLakeStoreFirewallRule [-Account] <String> [-Name] <String> [-StartIpAddress] <String>
 [-EndIpAddress] <String> [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7446-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f7446-105">DESCRIPTION</span></span>
<span data-ttu-id="f7446-106">Il cmdlet **Add-AzDataLakeStoreFirewallRule** aggiunge una regola del firewall all'account di data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="f7446-106">The **Add-AzDataLakeStoreFirewallRule** cmdlet adds a firewall rule to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="f7446-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f7446-107">EXAMPLES</span></span>

### <span data-ttu-id="f7446-108">Esempio 1: aggiungere una nuova regola del firewall a un account di data Lake Store</span><span class="sxs-lookup"><span data-stu-id="f7446-108">Example 1: Add a new firewall rule to a Data Lake Store account</span></span>
```
PS C:\> Add-AzDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyRule -StartIpAddress "127.0.0.1" -EndIpAddress "127.0.0.2"
```

<span data-ttu-id="f7446-109">In questo modo viene creata una nuova regola del firewall denominata "regola" in account "ContosoADL" con un intervallo IP di 127.0.0.1-127.0.0.2</span><span class="sxs-lookup"><span data-stu-id="f7446-109">This creates a new firewall rule called "MyRule" in account "ContosoADL" with an IP range of 127.0.0.1 - 127.0.0.2</span></span>

## <span data-ttu-id="f7446-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f7446-110">PARAMETERS</span></span>

### <span data-ttu-id="f7446-111">-Account</span><span class="sxs-lookup"><span data-stu-id="f7446-111">-Account</span></span>
<span data-ttu-id="f7446-112">L'account di data Lake Store per aggiungere la regola del firewall a</span><span class="sxs-lookup"><span data-stu-id="f7446-112">The Data Lake Store account to add the firewall rule to</span></span>

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

### <span data-ttu-id="f7446-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7446-113">-DefaultProfile</span></span>
<span data-ttu-id="f7446-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="f7446-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f7446-115">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="f7446-115">-EndIpAddress</span></span>
<span data-ttu-id="f7446-116">Fine dell'intervallo IP valido per la regola del firewall</span><span class="sxs-lookup"><span data-stu-id="f7446-116">The end of the valid ip range for the firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7446-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="f7446-117">-Name</span></span>
<span data-ttu-id="f7446-118">Nome della regola del firewall da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="f7446-118">The name of the firewall rule to add.</span></span>

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

### <span data-ttu-id="f7446-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7446-119">-ResourceGroupName</span></span>
<span data-ttu-id="f7446-120">Nome del gruppo di risorse in cui si trova l'account per aggiungere la regola del firewall.</span><span class="sxs-lookup"><span data-stu-id="f7446-120">Name of resource group under which the account to add the firewall rule is.</span></span>

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

### <span data-ttu-id="f7446-121">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="f7446-121">-StartIpAddress</span></span>
<span data-ttu-id="f7446-122">Inizio dell'intervallo IP valido per la regola del firewall</span><span class="sxs-lookup"><span data-stu-id="f7446-122">The start of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="f7446-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f7446-123">-Confirm</span></span>
<span data-ttu-id="f7446-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7446-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7446-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7446-125">-WhatIf</span></span>
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

### <span data-ttu-id="f7446-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7446-126">CommonParameters</span></span>
<span data-ttu-id="f7446-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7446-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7446-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7446-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7446-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f7446-129">INPUTS</span></span>

### <span data-ttu-id="f7446-130">System. String</span><span class="sxs-lookup"><span data-stu-id="f7446-130">System.String</span></span>

## <span data-ttu-id="f7446-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f7446-131">OUTPUTS</span></span>

### <span data-ttu-id="f7446-132">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f7446-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="f7446-133">Note</span><span class="sxs-lookup"><span data-stu-id="f7446-133">NOTES</span></span>

## <span data-ttu-id="f7446-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f7446-134">RELATED LINKS</span></span>