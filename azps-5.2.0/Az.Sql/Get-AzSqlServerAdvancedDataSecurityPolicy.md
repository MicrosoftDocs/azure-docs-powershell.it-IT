---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserveradvanceddatasecuritypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedDataSecurityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedDataSecurityPolicy.md
ms.openlocfilehash: 9776f4a569c2b8ac47d3bc8e478ce9fbfaccab01
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98350119"
---
# <span data-ttu-id="8451a-101">Get-AzSqlServerAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="8451a-101">Get-AzSqlServerAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="8451a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8451a-102">SYNOPSIS</span></span>
<span data-ttu-id="8451a-103">Ottiene i criteri di sicurezza dei dati avanzati di un server.</span><span class="sxs-lookup"><span data-stu-id="8451a-103">Gets Advanced Data Security policy of a server.</span></span>

## <span data-ttu-id="8451a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8451a-104">SYNTAX</span></span>

```
Get-AzSqlServerAdvancedDataSecurityPolicy [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8451a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8451a-105">DESCRIPTION</span></span>
<span data-ttu-id="8451a-106">Il cmdlet **Get-AzSqlServerAdvancedDataSecurityPolicy** recupera i criteri avanzati per la sicurezza dei dati di un server.</span><span class="sxs-lookup"><span data-stu-id="8451a-106">The **Get-AzSqlServerAdvancedDataSecurityPolicy** cmdlet retrieves the Advanced Data Security policy of a server.</span></span>

## <span data-ttu-id="8451a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8451a-107">EXAMPLES</span></span>

### <span data-ttu-id="8451a-108">Esempio 1: ottiene la sicurezza dei dati avanzata del server</span><span class="sxs-lookup"><span data-stu-id="8451a-108">Example 1: Gets server Advanced Data Security</span></span>
```powershell
PS C:\>  Get-AzSqlServerAdvancedDataSecurityPolicy `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

### <span data-ttu-id="8451a-109">Esempio 2: ottiene la sicurezza dei dati avanzata del server dalla risorsa server</span><span class="sxs-lookup"><span data-stu-id="8451a-109">Example 2: Gets server Advanced Data Security from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Get-AzSqlServerAdvancedDataSecurityPolicy

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

## <span data-ttu-id="8451a-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8451a-110">PARAMETERS</span></span>

### <span data-ttu-id="8451a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8451a-111">-DefaultProfile</span></span>
<span data-ttu-id="8451a-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8451a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8451a-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8451a-113">-InputObject</span></span>
<span data-ttu-id="8451a-114">L'oggetto server da usare con l'operazione Advanced Data Security Policy</span><span class="sxs-lookup"><span data-stu-id="8451a-114">The server object to use with Advanced Data Security policy operation</span></span>

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

### <span data-ttu-id="8451a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8451a-115">-ResourceGroupName</span></span>
<span data-ttu-id="8451a-116">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8451a-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="8451a-117">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="8451a-117">-ServerName</span></span>
<span data-ttu-id="8451a-118">Nome del server database SQL.</span><span class="sxs-lookup"><span data-stu-id="8451a-118">SQL Database server name.</span></span>

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

### <span data-ttu-id="8451a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8451a-119">CommonParameters</span></span>
<span data-ttu-id="8451a-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8451a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8451a-121">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8451a-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8451a-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8451a-122">INPUTS</span></span>

### <span data-ttu-id="8451a-123">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="8451a-123">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="8451a-124">System. String</span><span class="sxs-lookup"><span data-stu-id="8451a-124">System.String</span></span>

## <span data-ttu-id="8451a-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8451a-125">OUTPUTS</span></span>

### <span data-ttu-id="8451a-126">Microsoft. Azure. Commands. SQL. AdvancedThreatProtection. Model. ServerAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="8451a-126">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="8451a-127">Note</span><span class="sxs-lookup"><span data-stu-id="8451a-127">NOTES</span></span>

## <span data-ttu-id="8451a-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8451a-128">RELATED LINKS</span></span>
