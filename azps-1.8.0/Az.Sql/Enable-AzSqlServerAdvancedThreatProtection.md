---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/enable-azsqlserveradvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlServerAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlServerAdvancedThreatProtection.md
ms.openlocfilehash: aaaf417137bb1ec16150a2bf3d0ac88b64e70fae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677015"
---
# <span data-ttu-id="303f7-101">Enable-AzSqlServerAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="303f7-101">Enable-AzSqlServerAdvancedThreatProtection</span></span>

## <span data-ttu-id="303f7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="303f7-102">SYNOPSIS</span></span>
<span data-ttu-id="303f7-103">Consente la protezione avanzata delle minacce in un server.</span><span class="sxs-lookup"><span data-stu-id="303f7-103">Enables Advanced Threat Protection on a server.</span></span>

## <span data-ttu-id="303f7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="303f7-104">SYNTAX</span></span>

```
Enable-AzSqlServerAdvancedThreatProtection [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="303f7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="303f7-105">DESCRIPTION</span></span>
<span data-ttu-id="303f7-106">Il cmdlet **Enable-AzSqlServerAdvancedThreatProtection** consente la protezione avanzata delle minacce in un server.</span><span class="sxs-lookup"><span data-stu-id="303f7-106">The **Enable-AzSqlServerAdvancedThreatProtection** cmdlet enables Advanced Threat Protection on a server.</span></span>

## <span data-ttu-id="303f7-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="303f7-107">EXAMPLES</span></span>

### <span data-ttu-id="303f7-108">Esempio 1-abilitare la protezione avanzata delle minacce del server</span><span class="sxs-lookup"><span data-stu-id="303f7-108">Example 1 - Enable server Advanced Threat Protection</span></span>
```powershell
PS C:\>  Enable-AzSqlServerAdvancedThreatProtection `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

### <span data-ttu-id="303f7-109">Esempio 2-abilitare il server Advanced Threat Protection da Resource Server</span><span class="sxs-lookup"><span data-stu-id="303f7-109">Example 2 - Enable server Advanced Threat Protection from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Enable-AzSqlServerAdvancedThreatProtection

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

## <span data-ttu-id="303f7-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="303f7-110">PARAMETERS</span></span>

### <span data-ttu-id="303f7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="303f7-111">-DefaultProfile</span></span>
<span data-ttu-id="303f7-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="303f7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="303f7-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="303f7-113">-InputObject</span></span>
<span data-ttu-id="303f7-114">L'oggetto server da usare con l'operazione Advanced Threat Protection Policy</span><span class="sxs-lookup"><span data-stu-id="303f7-114">The server object to use with Advanced Threat Protection policy operation</span></span>

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

### <span data-ttu-id="303f7-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="303f7-115">-ResourceGroupName</span></span>
<span data-ttu-id="303f7-116">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="303f7-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="303f7-117">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="303f7-117">-ServerName</span></span>
<span data-ttu-id="303f7-118">Nome del server database SQL.</span><span class="sxs-lookup"><span data-stu-id="303f7-118">SQL Database server name.</span></span>

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

### <span data-ttu-id="303f7-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="303f7-119">-Confirm</span></span>
<span data-ttu-id="303f7-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="303f7-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="303f7-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="303f7-121">-WhatIf</span></span>
<span data-ttu-id="303f7-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="303f7-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="303f7-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="303f7-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="303f7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="303f7-124">CommonParameters</span></span>
<span data-ttu-id="303f7-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="303f7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="303f7-126">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="303f7-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="303f7-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="303f7-127">INPUTS</span></span>

### <span data-ttu-id="303f7-128">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="303f7-128">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="303f7-129">System. String</span><span class="sxs-lookup"><span data-stu-id="303f7-129">System.String</span></span>

## <span data-ttu-id="303f7-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="303f7-130">OUTPUTS</span></span>

### <span data-ttu-id="303f7-131">Microsoft. Azure. Commands. SQL. AdvancedThreatProtection. Model. ServerAdvancedThreatProtectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="303f7-131">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedThreatProtectionPolicyModel</span></span>

## <span data-ttu-id="303f7-132">Note</span><span class="sxs-lookup"><span data-stu-id="303f7-132">NOTES</span></span>

## <span data-ttu-id="303f7-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="303f7-133">RELATED LINKS</span></span>
