---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 9983EA1E-2515-4F5D-8476-8D0EE9837E88
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreFirewallRule.md
ms.openlocfilehash: 5c807c3d134768c7682b2216178eabd5a0771701
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180902"
---
# <span data-ttu-id="abde8-101">Set-AzDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="abde8-101">Set-AzDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="abde8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="abde8-102">SYNOPSIS</span></span>
<span data-ttu-id="abde8-103">Modifica la regola del firewall specificata nel Data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="abde8-103">Modifies the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="abde8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="abde8-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreFirewallRule [-Account] <String> [-Name] <String> [[-StartIpAddress] <String>]
 [[-EndIpAddress] <String>] [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="abde8-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="abde8-105">DESCRIPTION</span></span>
<span data-ttu-id="abde8-106">Il cmdlet **Set-AzDataLakeStoreFirewallRule** modifica la regola del firewall specificata nel Data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="abde8-106">The **Set-AzDataLakeStoreFirewallRule** cmdlet modifies the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="abde8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="abde8-107">EXAMPLES</span></span>

### <span data-ttu-id="abde8-108">Esempio 1: Aggiornare l'intervallo IP di inizio e di fine per una regola del firewall</span><span class="sxs-lookup"><span data-stu-id="abde8-108">Example 1: Update the start and end IP range for a firewall rule</span></span>
```
PS C:\> Set-AzDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule -StartIpAddress "127.0.0.1" -EndIpAddress "127.0.0.2"
```

<span data-ttu-id="abde8-109">Aggiorna la regola del firewall "MyFirewallRule" nell'account "ContosoADL" in modo che abbia un intervallo compreso tra 127.0.0.1 e 127.0.0.2</span><span class="sxs-lookup"><span data-stu-id="abde8-109">Updates the firewall rule "MyFirewallRule" in account "ContosoADL" to have a range of 127.0.0.1 - 127.0.0.2</span></span>

## <span data-ttu-id="abde8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="abde8-110">PARAMETERS</span></span>

### <span data-ttu-id="abde8-111">-Account</span><span class="sxs-lookup"><span data-stu-id="abde8-111">-Account</span></span>
<span data-ttu-id="abde8-112">Account Data Lake Store in cui aggiornare la regola del firewall in</span><span class="sxs-lookup"><span data-stu-id="abde8-112">The Data Lake Store account to update the firewall rule in</span></span>

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

### <span data-ttu-id="abde8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abde8-113">-DefaultProfile</span></span>
<span data-ttu-id="abde8-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="abde8-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="abde8-115">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="abde8-115">-EndIpAddress</span></span>
<span data-ttu-id="abde8-116">Fine dell'intervallo IP valido per la regola del firewall</span><span class="sxs-lookup"><span data-stu-id="abde8-116">The end of the valid ip range for the firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abde8-117">-Name</span><span class="sxs-lookup"><span data-stu-id="abde8-117">-Name</span></span>
<span data-ttu-id="abde8-118">Nome della regola del firewall.</span><span class="sxs-lookup"><span data-stu-id="abde8-118">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="abde8-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abde8-119">-ResourceGroupName</span></span>
<span data-ttu-id="abde8-120">Specifica il nome del gruppo di risorse che contiene l'account per cui aggiornare la regola del firewall.</span><span class="sxs-lookup"><span data-stu-id="abde8-120">Specifies the name of the resource group that contains the account to update the firewall rule for.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abde8-121">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="abde8-121">-StartIpAddress</span></span>
<span data-ttu-id="abde8-122">Inizio dell'intervallo IP valido per la regola del firewall</span><span class="sxs-lookup"><span data-stu-id="abde8-122">The start of the valid ip range for the firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abde8-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="abde8-123">-Confirm</span></span>
<span data-ttu-id="abde8-124">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="abde8-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="abde8-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="abde8-125">-WhatIf</span></span>
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

### <span data-ttu-id="abde8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abde8-126">CommonParameters</span></span>
<span data-ttu-id="abde8-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="abde8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abde8-128">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abde8-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abde8-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="abde8-129">INPUTS</span></span>

### <span data-ttu-id="abde8-130">System.String</span><span class="sxs-lookup"><span data-stu-id="abde8-130">System.String</span></span>

## <span data-ttu-id="abde8-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="abde8-131">OUTPUTS</span></span>

### <span data-ttu-id="abde8-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="abde8-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="abde8-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="abde8-133">NOTES</span></span>

## <span data-ttu-id="abde8-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="abde8-134">RELATED LINKS</span></span>
