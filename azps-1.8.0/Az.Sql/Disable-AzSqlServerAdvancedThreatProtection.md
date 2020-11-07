---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqlserveradvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerAdvancedThreatProtection.md
ms.openlocfilehash: d6a06c3f4c50e10522ed06e6b1cd4185c1ef6768
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677017"
---
# <span data-ttu-id="db532-101">Disable-AzSqlServerAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="db532-101">Disable-AzSqlServerAdvancedThreatProtection</span></span>

## <span data-ttu-id="db532-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="db532-102">SYNOPSIS</span></span>
<span data-ttu-id="db532-103">Disabilita la protezione avanzata delle minacce in un server.</span><span class="sxs-lookup"><span data-stu-id="db532-103">Disables Advanced Threat Protection on a server.</span></span>

## <span data-ttu-id="db532-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="db532-104">SYNTAX</span></span>

```
Disable-AzSqlServerAdvancedThreatProtection [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="db532-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="db532-105">DESCRIPTION</span></span>
<span data-ttu-id="db532-106">Il cmdlet **Disable-AzSqlServerAdvancedThreatProtection Disabilita** la protezione avanzata delle minacce in un server.</span><span class="sxs-lookup"><span data-stu-id="db532-106">The **Disable-AzSqlServerAdvancedThreatProtection** cmdlet disables Advanced Threat Protection on a server.</span></span>

## <span data-ttu-id="db532-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="db532-107">EXAMPLES</span></span>

### <span data-ttu-id="db532-108">Esempio 1-disabilitare la protezione avanzata delle minacce del server</span><span class="sxs-lookup"><span data-stu-id="db532-108">Example 1 - Disable server Advanced Threat Protection</span></span>
```powershell
PS C:\>  Disable-AzSqlServerAdvancedThreatProtection `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : False
```

### <span data-ttu-id="db532-109">Esempio 2-disabilitare la protezione avanzata delle minacce server dalla risorsa server</span><span class="sxs-lookup"><span data-stu-id="db532-109">Example 2 - Disable server Advanced Threat Protection from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Disable-AzSqlServerAdvancedThreatProtection

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : False
```

## <span data-ttu-id="db532-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="db532-110">PARAMETERS</span></span>

### <span data-ttu-id="db532-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db532-111">-DefaultProfile</span></span>
<span data-ttu-id="db532-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="db532-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db532-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="db532-113">-InputObject</span></span>
<span data-ttu-id="db532-114">L'oggetto server da usare con l'operazione Advanced Threat Protection Policy</span><span class="sxs-lookup"><span data-stu-id="db532-114">The server object to use with Advanced Threat Protection policy operation</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="db532-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db532-115">-ResourceGroupName</span></span>
<span data-ttu-id="db532-116">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="db532-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="db532-117">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="db532-117">-ServerName</span></span>
<span data-ttu-id="db532-118">Nome del server database SQL.</span><span class="sxs-lookup"><span data-stu-id="db532-118">SQL Database server name.</span></span>

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

### <span data-ttu-id="db532-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="db532-119">-Confirm</span></span>
<span data-ttu-id="db532-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db532-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db532-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db532-121">-WhatIf</span></span>
<span data-ttu-id="db532-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="db532-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="db532-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="db532-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db532-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db532-124">CommonParameters</span></span>
<span data-ttu-id="db532-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db532-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db532-126">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="db532-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db532-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="db532-127">INPUTS</span></span>

### <span data-ttu-id="db532-128">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="db532-128">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="db532-129">System. String</span><span class="sxs-lookup"><span data-stu-id="db532-129">System.String</span></span>

## <span data-ttu-id="db532-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="db532-130">OUTPUTS</span></span>

### <span data-ttu-id="db532-131">Microsoft. Azure. Commands. SQL. AdvancedThreatProtection. Model. ServerAdvancedThreatProtectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="db532-131">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedThreatProtectionPolicyModel</span></span>

## <span data-ttu-id="db532-132">Note</span><span class="sxs-lookup"><span data-stu-id="db532-132">NOTES</span></span>

## <span data-ttu-id="db532-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="db532-133">RELATED LINKS</span></span>
