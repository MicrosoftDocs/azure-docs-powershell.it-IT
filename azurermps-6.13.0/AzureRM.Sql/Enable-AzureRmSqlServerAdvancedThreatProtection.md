---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/enable-azurermsqlserveradvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Enable-AzureRmSqlServerAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Enable-AzureRmSqlServerAdvancedThreatProtection.md
ms.openlocfilehash: 1276ba100a795ca113f1f09064bc46dfdfddf39b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687575"
---
# <span data-ttu-id="5fdb3-101">Enable-AzureRmSqlServerAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="5fdb3-101">Enable-AzureRmSqlServerAdvancedThreatProtection</span></span>

## <span data-ttu-id="5fdb3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5fdb3-102">SYNOPSIS</span></span>
<span data-ttu-id="5fdb3-103">Consente la protezione avanzata delle minacce in un server.</span><span class="sxs-lookup"><span data-stu-id="5fdb3-103">Enables Advanced Threat Protection on a server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5fdb3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5fdb3-104">SYNTAX</span></span>

```
Enable-AzureRmSqlServerAdvancedThreatProtection [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5fdb3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5fdb3-105">DESCRIPTION</span></span>
<span data-ttu-id="5fdb3-106">Il cmdlet **Enable-AzureRmSqlServerAdvancedThreatProtection** consente la protezione avanzata delle minacce in un server.</span><span class="sxs-lookup"><span data-stu-id="5fdb3-106">The **Enable-AzureRmSqlServerAdvancedThreatProtection** cmdlet enables Advanced Threat Protection on a server.</span></span>

## <span data-ttu-id="5fdb3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5fdb3-107">EXAMPLES</span></span>

### <span data-ttu-id="5fdb3-108">Esempio 1-abilitare la protezione avanzata delle minacce del server</span><span class="sxs-lookup"><span data-stu-id="5fdb3-108">Example 1 - Enable server Advanced Threat Protection</span></span>
```powershell
PS C:\>  Enable-AzureRmSqlServerAdvancedThreatProtection `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

### <span data-ttu-id="5fdb3-109">Esempio 2-abilitare il server Advanced Threat Protection da Resource Server</span><span class="sxs-lookup"><span data-stu-id="5fdb3-109">Example 2 - Enable server Advanced Threat Protection from server resource</span></span>
```powershell
PS C:\>  Get-AzureRmSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Enable-AzureRmSqlServerAdvancedThreatProtection

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

## <span data-ttu-id="5fdb3-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5fdb3-110">PARAMETERS</span></span>

### <span data-ttu-id="5fdb3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fdb3-111">-DefaultProfile</span></span>
<span data-ttu-id="5fdb3-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5fdb3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5fdb3-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5fdb3-113">-InputObject</span></span>
<span data-ttu-id="5fdb3-114">L'oggetto server da usare con l'operazione Advanced Threat Protection Policy</span><span class="sxs-lookup"><span data-stu-id="5fdb3-114">The server object to use with Advanced Threat Protection policy operation</span></span>

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

### <span data-ttu-id="5fdb3-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fdb3-115">-ResourceGroupName</span></span>
<span data-ttu-id="5fdb3-116">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5fdb3-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="5fdb3-117">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="5fdb3-117">-ServerName</span></span>
<span data-ttu-id="5fdb3-118">Nome del server database SQL.</span><span class="sxs-lookup"><span data-stu-id="5fdb3-118">SQL Database server name.</span></span>

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

### <span data-ttu-id="5fdb3-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5fdb3-119">-Confirm</span></span>
<span data-ttu-id="5fdb3-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5fdb3-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5fdb3-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5fdb3-121">-WhatIf</span></span>
<span data-ttu-id="5fdb3-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5fdb3-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5fdb3-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5fdb3-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5fdb3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fdb3-124">CommonParameters</span></span>
<span data-ttu-id="5fdb3-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5fdb3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fdb3-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5fdb3-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fdb3-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5fdb3-127">INPUTS</span></span>

### <span data-ttu-id="5fdb3-128">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="5fdb3-128">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>
<span data-ttu-id="5fdb3-129">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5fdb3-129">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="5fdb3-130">System. String</span><span class="sxs-lookup"><span data-stu-id="5fdb3-130">System.String</span></span>

## <span data-ttu-id="5fdb3-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5fdb3-131">OUTPUTS</span></span>

### <span data-ttu-id="5fdb3-132">Microsoft. Azure. Commands. SQL. AdvancedThreatProtection. Model. ServerAdvancedThreatProtectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="5fdb3-132">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedThreatProtectionPolicyModel</span></span>

## <span data-ttu-id="5fdb3-133">Note</span><span class="sxs-lookup"><span data-stu-id="5fdb3-133">NOTES</span></span>

## <span data-ttu-id="5fdb3-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5fdb3-134">RELATED LINKS</span></span>
