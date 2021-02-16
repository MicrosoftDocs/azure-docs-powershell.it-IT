---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: C6FD4734-720C-4C8C-9B58-EDB331DD6415
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/add-azdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreFirewallRule.md
ms.openlocfilehash: a13125695ab5f4c57ab2e7013d64fff376643076
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194703"
---
# <span data-ttu-id="cce1f-101">Add-AzDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="cce1f-101">Add-AzDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="cce1f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cce1f-102">SYNOPSIS</span></span>
<span data-ttu-id="cce1f-103">Aggiunge una regola del firewall all'account Data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="cce1f-103">Adds a firewall rule to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="cce1f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cce1f-104">SYNTAX</span></span>

```
Add-AzDataLakeStoreFirewallRule [-Account] <String> [-Name] <String> [-StartIpAddress] <String>
 [-EndIpAddress] <String> [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cce1f-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="cce1f-105">DESCRIPTION</span></span>
<span data-ttu-id="cce1f-106">Il cmdlet **Add-AzDataLakeStoreFirewallRule** aggiunge una regola del firewall all'account Data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="cce1f-106">The **Add-AzDataLakeStoreFirewallRule** cmdlet adds a firewall rule to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="cce1f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cce1f-107">EXAMPLES</span></span>

### <span data-ttu-id="cce1f-108">Esempio 1: Aggiungere una nuova regola del firewall a un account Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="cce1f-108">Example 1: Add a new firewall rule to a Data Lake Store account</span></span>
```
PS C:\> Add-AzDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyRule -StartIpAddress "127.0.0.1" -EndIpAddress "127.0.0.2"
```

<span data-ttu-id="cce1f-109">Viene creata una nuova regola del firewall denominata "MyRule" nell'account "ContosoADL" con un intervallo IP compreso tra 127.0.0.1 e 127.0.0.2.</span><span class="sxs-lookup"><span data-stu-id="cce1f-109">This creates a new firewall rule called "MyRule" in account "ContosoADL" with an IP range of 127.0.0.1 - 127.0.0.2</span></span>

## <span data-ttu-id="cce1f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cce1f-110">PARAMETERS</span></span>

### <span data-ttu-id="cce1f-111">-Account</span><span class="sxs-lookup"><span data-stu-id="cce1f-111">-Account</span></span>
<span data-ttu-id="cce1f-112">Account Data Lake Store a cui aggiungere la regola del firewall</span><span class="sxs-lookup"><span data-stu-id="cce1f-112">The Data Lake Store account to add the firewall rule to</span></span>

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

### <span data-ttu-id="cce1f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cce1f-113">-DefaultProfile</span></span>
<span data-ttu-id="cce1f-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="cce1f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cce1f-115">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="cce1f-115">-EndIpAddress</span></span>
<span data-ttu-id="cce1f-116">Fine dell'intervallo IP valido per la regola del firewall</span><span class="sxs-lookup"><span data-stu-id="cce1f-116">The end of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="cce1f-117">-Name</span><span class="sxs-lookup"><span data-stu-id="cce1f-117">-Name</span></span>
<span data-ttu-id="cce1f-118">Nome della regola del firewall da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="cce1f-118">The name of the firewall rule to add.</span></span>

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

### <span data-ttu-id="cce1f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cce1f-119">-ResourceGroupName</span></span>
<span data-ttu-id="cce1f-120">Nome del gruppo di risorse in cui si trova l'account in cui aggiungere la regola del firewall.</span><span class="sxs-lookup"><span data-stu-id="cce1f-120">Name of resource group under which the account to add the firewall rule is.</span></span>

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

### <span data-ttu-id="cce1f-121">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="cce1f-121">-StartIpAddress</span></span>
<span data-ttu-id="cce1f-122">Inizio dell'intervallo IP valido per la regola del firewall</span><span class="sxs-lookup"><span data-stu-id="cce1f-122">The start of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="cce1f-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cce1f-123">-Confirm</span></span>
<span data-ttu-id="cce1f-124">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cce1f-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cce1f-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cce1f-125">-WhatIf</span></span>
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

### <span data-ttu-id="cce1f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cce1f-126">CommonParameters</span></span>
<span data-ttu-id="cce1f-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cce1f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cce1f-128">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cce1f-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cce1f-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="cce1f-129">INPUTS</span></span>

### <span data-ttu-id="cce1f-130">System.String</span><span class="sxs-lookup"><span data-stu-id="cce1f-130">System.String</span></span>

## <span data-ttu-id="cce1f-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cce1f-131">OUTPUTS</span></span>

### <span data-ttu-id="cce1f-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="cce1f-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="cce1f-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="cce1f-133">NOTES</span></span>

## <span data-ttu-id="cce1f-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cce1f-134">RELATED LINKS</span></span>
