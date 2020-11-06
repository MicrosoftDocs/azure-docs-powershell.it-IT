---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserveradvancedthreatprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAdvancedThreatProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAdvancedThreatProtectionPolicy.md
ms.openlocfilehash: 16762b56995b90422c78ad6dc5dd87461c0a8317
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518512"
---
# <span data-ttu-id="64acf-101">Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="64acf-101">Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>

## <span data-ttu-id="64acf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="64acf-102">SYNOPSIS</span></span>
<span data-ttu-id="64acf-103">Ottiene i criteri avanzati per la protezione delle minacce di un server.</span><span class="sxs-lookup"><span data-stu-id="64acf-103">Gets Advanced Threat Protection policy of a server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="64acf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="64acf-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerAdvancedThreatProtectionPolicy [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="64acf-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="64acf-105">DESCRIPTION</span></span>
<span data-ttu-id="64acf-106">Il cmdlet **Get-AzureRmSqlServerAdvancedThreatProtectionPolicy** Retrives i criteri avanzati per la protezione delle minacce di un server.</span><span class="sxs-lookup"><span data-stu-id="64acf-106">The **Get-AzureRmSqlServerAdvancedThreatProtectionPolicy** cmdlet retrives the Advanced Threat Protection policy of a server.</span></span>

## <span data-ttu-id="64acf-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="64acf-107">EXAMPLES</span></span>

### <span data-ttu-id="64acf-108">Esempio 1-Ottiene la protezione avanzata dalle minacce del server</span><span class="sxs-lookup"><span data-stu-id="64acf-108">Example 1 - Gets server Advanced Threat Protection</span></span>
```powershell
PS C:\>  Get-AzureRmSqlServerAdvancedThreatProtectionPolicy `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

### <span data-ttu-id="64acf-109">Esempio 2-ottiene la protezione avanzata dalle minacce del server dalla risorsa server</span><span class="sxs-lookup"><span data-stu-id="64acf-109">Example 2 - Gets server Advanced Threat Protection from server resource</span></span>
```powershell
PS C:\>  Get-AzureRmSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Get-AzureRmSqlServerAdvancedThreatProtectionPolicy

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

## <span data-ttu-id="64acf-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="64acf-110">PARAMETERS</span></span>

### <span data-ttu-id="64acf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64acf-111">-DefaultProfile</span></span>
<span data-ttu-id="64acf-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="64acf-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64acf-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="64acf-113">-InputObject</span></span>
<span data-ttu-id="64acf-114">L'oggetto server da usare con l'operazione Advanced Threat Protection Policy</span><span class="sxs-lookup"><span data-stu-id="64acf-114">The server object to use with Advanced Threat Protection policy operation</span></span>

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

### <span data-ttu-id="64acf-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64acf-115">-ResourceGroupName</span></span>
<span data-ttu-id="64acf-116">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="64acf-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="64acf-117">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="64acf-117">-ServerName</span></span>
<span data-ttu-id="64acf-118">Nome del server database SQL.</span><span class="sxs-lookup"><span data-stu-id="64acf-118">SQL Database server name.</span></span>

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

### <span data-ttu-id="64acf-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64acf-119">CommonParameters</span></span>
<span data-ttu-id="64acf-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64acf-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64acf-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64acf-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64acf-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="64acf-122">INPUTS</span></span>

### <span data-ttu-id="64acf-123">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="64acf-123">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>
<span data-ttu-id="64acf-124">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="64acf-124">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="64acf-125">System. String</span><span class="sxs-lookup"><span data-stu-id="64acf-125">System.String</span></span>

## <span data-ttu-id="64acf-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="64acf-126">OUTPUTS</span></span>

### <span data-ttu-id="64acf-127">Microsoft. Azure. Commands. SQL. AdvancedThreatProtection. Model. ServerAdvancedThreatProtectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="64acf-127">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedThreatProtectionPolicyModel</span></span>

## <span data-ttu-id="64acf-128">Note</span><span class="sxs-lookup"><span data-stu-id="64acf-128">NOTES</span></span>

## <span data-ttu-id="64acf-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="64acf-129">RELATED LINKS</span></span>
