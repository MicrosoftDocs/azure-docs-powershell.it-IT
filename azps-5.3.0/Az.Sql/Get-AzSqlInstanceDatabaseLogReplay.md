---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Get-AzSqlInstanceDatabaseLogReplay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseLogReplay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseLogReplay.md
ms.openlocfilehash: 7e37dcceb45370e4956fb59912a50a501fe271c1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98475651"
---
# <span data-ttu-id="9b0ff-101">Get-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="9b0ff-101">Get-AzSqlInstanceDatabaseLogReplay</span></span>

## <span data-ttu-id="9b0ff-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9b0ff-102">SYNOPSIS</span></span>
<span data-ttu-id="9b0ff-103">Ottiene lo stato del servizio di riproduzione del log.</span><span class="sxs-lookup"><span data-stu-id="9b0ff-103">Gets the Log Replay service status.</span></span>

## <span data-ttu-id="9b0ff-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9b0ff-104">SYNTAX</span></span>

```
Get-AzSqlInstanceDatabaseLogReplay [[-Name] <String>] [-InstanceName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9b0ff-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9b0ff-105">DESCRIPTION</span></span>
<span data-ttu-id="9b0ff-106">Il cmdlet **Get-AzSqlInstanceDatabaseLogReplay** ottiene lo stato del servizio di riproduzione del log nel database specifico.</span><span class="sxs-lookup"><span data-stu-id="9b0ff-106">The **Get-AzSqlInstanceDatabaseLogReplay** cmdlet gets the Log Replay service status on the given database.</span></span>

## <span data-ttu-id="9b0ff-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9b0ff-107">EXAMPLES</span></span>

### <span data-ttu-id="9b0ff-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9b0ff-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName"
```

<span data-ttu-id="9b0ff-109">Questo comando otterrà lo stato del servizio di riproduzione del log nel database specifico.</span><span class="sxs-lookup"><span data-stu-id="9b0ff-109">This command will get log replay service status on the given database.</span></span>

## <span data-ttu-id="9b0ff-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9b0ff-110">PARAMETERS</span></span>

### <span data-ttu-id="9b0ff-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b0ff-111">-DefaultProfile</span></span>
<span data-ttu-id="9b0ff-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9b0ff-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b0ff-113">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="9b0ff-113">-InstanceName</span></span>
<span data-ttu-id="9b0ff-114">Nome dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="9b0ff-114">The name of the instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ManagedInstanceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b0ff-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="9b0ff-115">-Name</span></span>
<span data-ttu-id="9b0ff-116">Nome del database dell'istanza da recuperare.</span><span class="sxs-lookup"><span data-stu-id="9b0ff-116">The name of the instance database to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: InstanceDatabaseName

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b0ff-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b0ff-117">-ResourceGroupName</span></span>
<span data-ttu-id="9b0ff-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9b0ff-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="9b0ff-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b0ff-119">CommonParameters</span></span>
<span data-ttu-id="9b0ff-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b0ff-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b0ff-121">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9b0ff-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b0ff-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9b0ff-122">INPUTS</span></span>

### <span data-ttu-id="9b0ff-123">System. String</span><span class="sxs-lookup"><span data-stu-id="9b0ff-123">System.String</span></span>

## <span data-ttu-id="9b0ff-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9b0ff-124">OUTPUTS</span></span>

### <span data-ttu-id="9b0ff-125">Microsoft. Azure. Commands. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseRestoreDetailsResultModel</span><span class="sxs-lookup"><span data-stu-id="9b0ff-125">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseRestoreDetailsResultModel</span></span>

## <span data-ttu-id="9b0ff-126">Note</span><span class="sxs-lookup"><span data-stu-id="9b0ff-126">NOTES</span></span>

## <span data-ttu-id="9b0ff-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9b0ff-127">RELATED LINKS</span></span>
