---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqlserveradvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerAdvancedDataSecurity.md
ms.openlocfilehash: 482a620552457993795ba03e2da9367df5efa614
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93864105"
---
# <span data-ttu-id="b46fb-101">Disable-AzSqlServerAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="b46fb-101">Disable-AzSqlServerAdvancedDataSecurity</span></span>

## <span data-ttu-id="b46fb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b46fb-102">SYNOPSIS</span></span>
<span data-ttu-id="b46fb-103">Disabilita la sicurezza avanzata dei dati in un server.</span><span class="sxs-lookup"><span data-stu-id="b46fb-103">Disables Advanced Data Security on a server.</span></span>

## <span data-ttu-id="b46fb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b46fb-104">SYNTAX</span></span>

```
Disable-AzSqlServerAdvancedDataSecurity [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b46fb-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b46fb-105">DESCRIPTION</span></span>
<span data-ttu-id="b46fb-106">Il cmdlet **Disable-AzSqlServerAdvancedDataSecurity Disabilita** la sicurezza dei dati avanzata in un server.</span><span class="sxs-lookup"><span data-stu-id="b46fb-106">The **Disable-AzSqlServerAdvancedDataSecurity** cmdlet disables Advanced Data Security on a server.</span></span>

## <span data-ttu-id="b46fb-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b46fb-107">EXAMPLES</span></span>

### <span data-ttu-id="b46fb-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b46fb-108">Example 1</span></span>
### <span data-ttu-id="b46fb-109">Esempio 1-disabilitare la sicurezza dei dati avanzata del server</span><span class="sxs-lookup"><span data-stu-id="b46fb-109">Example 1 - Disable server Advanced Data Security</span></span>
```powershell
PS C:\>  Disable-AzSqlServerAdvancedDataSecurity `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : False
```

### <span data-ttu-id="b46fb-110">Esempio 2-disabilitare la sicurezza dei dati avanzata del server dalla risorsa server</span><span class="sxs-lookup"><span data-stu-id="b46fb-110">Example 2 - Disable server Advanced Data Security from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Disable-AzSqlServerAdvancedDataSecurity

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : False
```

## <span data-ttu-id="b46fb-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b46fb-111">PARAMETERS</span></span>

### <span data-ttu-id="b46fb-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b46fb-112">-DefaultProfile</span></span>
<span data-ttu-id="b46fb-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b46fb-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b46fb-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b46fb-114">-InputObject</span></span>
<span data-ttu-id="b46fb-115">L'oggetto server da usare con l'operazione Advanced Data Security Policy</span><span class="sxs-lookup"><span data-stu-id="b46fb-115">The server object to use with Advanced Data Security policy operation</span></span>

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

### <span data-ttu-id="b46fb-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b46fb-116">-ResourceGroupName</span></span>
<span data-ttu-id="b46fb-117">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b46fb-117">The name of the resource group.</span></span>

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

### <span data-ttu-id="b46fb-118">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="b46fb-118">-ServerName</span></span>
<span data-ttu-id="b46fb-119">Nome del server database SQL.</span><span class="sxs-lookup"><span data-stu-id="b46fb-119">SQL Database server name.</span></span>

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

### <span data-ttu-id="b46fb-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b46fb-120">-Confirm</span></span>
<span data-ttu-id="b46fb-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b46fb-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b46fb-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b46fb-122">-WhatIf</span></span>
<span data-ttu-id="b46fb-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b46fb-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b46fb-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b46fb-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b46fb-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b46fb-125">CommonParameters</span></span>
<span data-ttu-id="b46fb-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b46fb-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b46fb-127">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b46fb-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b46fb-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b46fb-128">INPUTS</span></span>

### <span data-ttu-id="b46fb-129">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="b46fb-129">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="b46fb-130">System. String</span><span class="sxs-lookup"><span data-stu-id="b46fb-130">System.String</span></span>

## <span data-ttu-id="b46fb-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b46fb-131">OUTPUTS</span></span>

### <span data-ttu-id="b46fb-132">Microsoft. Azure. Commands. SQL. AdvancedThreatProtection. Model. ServerAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="b46fb-132">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="b46fb-133">Note</span><span class="sxs-lookup"><span data-stu-id="b46fb-133">NOTES</span></span>

## <span data-ttu-id="b46fb-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b46fb-134">RELATED LINKS</span></span>
