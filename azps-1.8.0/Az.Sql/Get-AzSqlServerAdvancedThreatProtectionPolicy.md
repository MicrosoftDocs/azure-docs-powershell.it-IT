---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserveradvancedthreatprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedThreatProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedThreatProtectionPolicy.md
ms.openlocfilehash: dce8018e97e01c10356e77d321d564690cc03f71
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676914"
---
# <span data-ttu-id="64ecf-101">Get-AzSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="64ecf-101">Get-AzSqlServerAdvancedThreatProtectionPolicy</span></span>

## <span data-ttu-id="64ecf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="64ecf-102">SYNOPSIS</span></span>
<span data-ttu-id="64ecf-103">Ottiene i criteri avanzati per la protezione delle minacce di un server.</span><span class="sxs-lookup"><span data-stu-id="64ecf-103">Gets Advanced Threat Protection policy of a server.</span></span>

## <span data-ttu-id="64ecf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="64ecf-104">SYNTAX</span></span>

```
Get-AzSqlServerAdvancedThreatProtectionPolicy [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="64ecf-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="64ecf-105">DESCRIPTION</span></span>
<span data-ttu-id="64ecf-106">Il cmdlet **Get-AzSqlServerAdvancedThreatProtectionPolicy** Retrives i criteri avanzati per la protezione delle minacce di un server.</span><span class="sxs-lookup"><span data-stu-id="64ecf-106">The **Get-AzSqlServerAdvancedThreatProtectionPolicy** cmdlet retrives the Advanced Threat Protection policy of a server.</span></span>

## <span data-ttu-id="64ecf-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="64ecf-107">EXAMPLES</span></span>

### <span data-ttu-id="64ecf-108">Esempio 1-Ottiene la protezione avanzata dalle minacce del server</span><span class="sxs-lookup"><span data-stu-id="64ecf-108">Example 1 - Gets server Advanced Threat Protection</span></span>
```powershell
PS C:\>  Get-AzSqlServerAdvancedThreatProtectionPolicy `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

### <span data-ttu-id="64ecf-109">Esempio 2-ottiene la protezione avanzata dalle minacce del server dalla risorsa server</span><span class="sxs-lookup"><span data-stu-id="64ecf-109">Example 2 - Gets server Advanced Threat Protection from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Get-AzSqlServerAdvancedThreatProtectionPolicy

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

## <span data-ttu-id="64ecf-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="64ecf-110">PARAMETERS</span></span>

### <span data-ttu-id="64ecf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64ecf-111">-DefaultProfile</span></span>
<span data-ttu-id="64ecf-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="64ecf-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64ecf-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="64ecf-113">-InputObject</span></span>
<span data-ttu-id="64ecf-114">L'oggetto server da usare con l'operazione Advanced Threat Protection Policy</span><span class="sxs-lookup"><span data-stu-id="64ecf-114">The server object to use with Advanced Threat Protection policy operation</span></span>

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

### <span data-ttu-id="64ecf-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64ecf-115">-ResourceGroupName</span></span>
<span data-ttu-id="64ecf-116">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="64ecf-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="64ecf-117">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="64ecf-117">-ServerName</span></span>
<span data-ttu-id="64ecf-118">Nome del server database SQL.</span><span class="sxs-lookup"><span data-stu-id="64ecf-118">SQL Database server name.</span></span>

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

### <span data-ttu-id="64ecf-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64ecf-119">CommonParameters</span></span>
<span data-ttu-id="64ecf-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64ecf-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64ecf-121">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="64ecf-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64ecf-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="64ecf-122">INPUTS</span></span>

### <span data-ttu-id="64ecf-123">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="64ecf-123">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="64ecf-124">System. String</span><span class="sxs-lookup"><span data-stu-id="64ecf-124">System.String</span></span>

## <span data-ttu-id="64ecf-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="64ecf-125">OUTPUTS</span></span>

### <span data-ttu-id="64ecf-126">Microsoft. Azure. Commands. SQL. AdvancedThreatProtection. Model. ServerAdvancedThreatProtectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="64ecf-126">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedThreatProtectionPolicyModel</span></span>

## <span data-ttu-id="64ecf-127">Note</span><span class="sxs-lookup"><span data-stu-id="64ecf-127">NOTES</span></span>

## <span data-ttu-id="64ecf-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="64ecf-128">RELATED LINKS</span></span>
