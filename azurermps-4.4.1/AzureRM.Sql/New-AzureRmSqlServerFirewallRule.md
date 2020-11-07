---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 51AF8EFB-F0C1-41E0-BBC5-E48FB1B8672C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerFirewallRule.md
ms.openlocfilehash: b40ac97f5658758fa77900dfc31da5f77fb5d0e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685649"
---
# <span data-ttu-id="d9d03-101">New-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d9d03-101">New-AzureRmSqlServerFirewallRule</span></span>

## <span data-ttu-id="d9d03-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d9d03-102">SYNOPSIS</span></span>
<span data-ttu-id="d9d03-103">Crea una regola del firewall per un server di database SQL.</span><span class="sxs-lookup"><span data-stu-id="d9d03-103">Creates a firewall rule for a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d9d03-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d9d03-104">SYNTAX</span></span>

### <span data-ttu-id="d9d03-105">UserSpecifiedRuleSet</span><span class="sxs-lookup"><span data-stu-id="d9d03-105">UserSpecifiedRuleSet</span></span>
```
New-AzureRmSqlServerFirewallRule -FirewallRuleName <String> -StartIpAddress <String> -EndIpAddress <String>
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9d03-106">AzureIpRuleSet</span><span class="sxs-lookup"><span data-stu-id="d9d03-106">AzureIpRuleSet</span></span>
```
New-AzureRmSqlServerFirewallRule [-AllowAllAzureIPs] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9d03-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d9d03-107">DESCRIPTION</span></span>
<span data-ttu-id="d9d03-108">Il cmdlet **New-AzureRmSqlServerFirewallRule** crea una regola del firewall per il server di database SQL di Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="d9d03-108">The **New-AzureRmSqlServerFirewallRule** cmdlet creates a firewall rule for the specified Azure SQL Database server.</span></span>

## <span data-ttu-id="d9d03-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d9d03-109">EXAMPLES</span></span>

### <span data-ttu-id="d9d03-110">Esempio 1: creare una regola del firewall</span><span class="sxs-lookup"><span data-stu-id="d9d03-110">Example 1: Create a firewall rule</span></span>
```
PS C:\>New-AzureRmSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -FirewallRuleName "Rule01" -StartIpAddress "192.168.0.198" -EndIpAddress "192.168.0.199"
ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 192.168.0.198
EndIpAddress      : 192.168.0.199
FirewallRuleName  : Rule01
```

<span data-ttu-id="d9d03-111">Questo comando crea una regola del firewall denominata Rule01 nel server denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="d9d03-111">This command creates a firewall rule named Rule01 on the server named Server01.</span></span>
<span data-ttu-id="d9d03-112">La regola include gli indirizzi IP iniziali e finali specificati.</span><span class="sxs-lookup"><span data-stu-id="d9d03-112">The rule includes the specified start and end IP addresses.</span></span>

### <span data-ttu-id="d9d03-113">Esempio 2: creare una regola del firewall che consente a tutti gli indirizzi IP di Azure di accedere al server</span><span class="sxs-lookup"><span data-stu-id="d9d03-113">Example 2: Create a firewall rule that allows all Azure IP addresses to access the server</span></span>
```
PS C:\>New-AzureRmSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -AllowAllAzureIPs
```

<span data-ttu-id="d9d03-114">Questo comando crea una regola del firewall nel server denominata Server01 che appartiene al gruppo di risorse denominato ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="d9d03-114">This command creates a firewall rule on the server named Server01 that belongs to the resource group named ResourceGroup01.</span></span>
<span data-ttu-id="d9d03-115">Poiché viene usato il parametro *AllowAllAzureIPs* , la regola del firewall consente a tutti gli indirizzi IP di Azure di accedere al server.</span><span class="sxs-lookup"><span data-stu-id="d9d03-115">Since the *AllowAllAzureIPs* parameter is used, the firewall rule allows all Azure IP addresses to access the server.</span></span>

## <span data-ttu-id="d9d03-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d9d03-116">PARAMETERS</span></span>

### <span data-ttu-id="d9d03-117">-AllowAllAzureIPs</span><span class="sxs-lookup"><span data-stu-id="d9d03-117">-AllowAllAzureIPs</span></span>
<span data-ttu-id="d9d03-118">Indica che questa regola del firewall consente a tutti gli indirizzi IP di Azure di accedere al server.</span><span class="sxs-lookup"><span data-stu-id="d9d03-118">Indicates that this firewall rule allows all Azure IP addresses to access the server.</span></span>
<span data-ttu-id="d9d03-119">Non è possibile usare questo parametro se si intende usare i parametri *FirewallRuleName* , *StartIpAddress* e *EndIpAddress* .</span><span class="sxs-lookup"><span data-stu-id="d9d03-119">You cannot use this parameter if you intend to use the *FirewallRuleName* , *StartIpAddress* , and *EndIpAddress* parameters.</span></span>
<span data-ttu-id="d9d03-120">Se vuoi consentire ad Azure IPs di accedere al server, questo parametro deve essere usato in una chiamata cmdlet separata che non usa i parametri *FirewallRuleName* , *StartIpAddress* e *EndIpAddress* .</span><span class="sxs-lookup"><span data-stu-id="d9d03-120">If you want to allow Azure IPs to access the server, this parameter should be used in a separate cmdlet call that does not use the *FirewallRuleName* , *StartIpAddress* , and *EndIpAddress* parameters.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureIpRuleSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9d03-121">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="d9d03-121">-EndIpAddress</span></span>
<span data-ttu-id="d9d03-122">Specifica il valore finale dell'intervallo di indirizzi IP per la regola.</span><span class="sxs-lookup"><span data-stu-id="d9d03-122">Specifies the end value of the IP address range for this rule.</span></span>

```yaml
Type: System.String
Parameter Sets: UserSpecifiedRuleSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9d03-123">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="d9d03-123">-FirewallRuleName</span></span>
<span data-ttu-id="d9d03-124">Specifica il nome della nuova regola del firewall.</span><span class="sxs-lookup"><span data-stu-id="d9d03-124">Specifies the name of the new firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: UserSpecifiedRuleSet
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9d03-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9d03-125">-ResourceGroupName</span></span>
<span data-ttu-id="d9d03-126">Specifica il nome di un gruppo di risorse a cui è assegnato il server.</span><span class="sxs-lookup"><span data-stu-id="d9d03-126">Specifies the name of a resource group to which the server is assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9d03-127">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="d9d03-127">-ServerName</span></span>
<span data-ttu-id="d9d03-128">Specifica il nome di un server.</span><span class="sxs-lookup"><span data-stu-id="d9d03-128">Specifies the name of a server.</span></span>
<span data-ttu-id="d9d03-129">Specificare il nome del server e non il nome DNS completo.</span><span class="sxs-lookup"><span data-stu-id="d9d03-129">Specify the server name, not the fully qualified DNS name.</span></span>

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

### <span data-ttu-id="d9d03-130">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="d9d03-130">-StartIpAddress</span></span>
<span data-ttu-id="d9d03-131">Specifica il valore iniziale dell'intervallo di indirizzi IP per la regola del firewall.</span><span class="sxs-lookup"><span data-stu-id="d9d03-131">Specifies the start value of the IP address range for the firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: UserSpecifiedRuleSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9d03-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d9d03-132">-Confirm</span></span>
<span data-ttu-id="d9d03-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9d03-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9d03-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9d03-134">-WhatIf</span></span>
<span data-ttu-id="d9d03-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d9d03-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9d03-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d9d03-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9d03-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9d03-137">-DefaultProfile</span></span>
<span data-ttu-id="d9d03-138">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d9d03-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d9d03-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9d03-139">CommonParameters</span></span>
<span data-ttu-id="d9d03-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9d03-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9d03-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9d03-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9d03-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d9d03-142">INPUTS</span></span>

## <span data-ttu-id="d9d03-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d9d03-143">OUTPUTS</span></span>

### <span data-ttu-id="d9d03-144">Microsoft. Azure. Commands. SQL. FirewallRule. Model. AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="d9d03-144">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="d9d03-145">Note</span><span class="sxs-lookup"><span data-stu-id="d9d03-145">NOTES</span></span>

## <span data-ttu-id="d9d03-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d9d03-146">RELATED LINKS</span></span>

[<span data-ttu-id="d9d03-147">Get-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d9d03-147">Get-AzureRmSqlServerFirewallRule</span></span>](./Get-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="d9d03-148">Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d9d03-148">Remove-AzureRmSqlServerFirewallRule</span></span>](./Remove-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="d9d03-149">Set-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d9d03-149">Set-AzureRmSqlServerFirewallRule</span></span>](./Set-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="d9d03-150">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="d9d03-150">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


