---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAuditing.md
ms.openlocfilehash: 636b3602c6dafc2c00e02e19aa35d0e91c278137
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512244"
---
# <span data-ttu-id="f7442-101">Get-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="f7442-101">Get-AzureRmSqlServerAuditing</span></span>

## <span data-ttu-id="f7442-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f7442-102">SYNOPSIS</span></span>
<span data-ttu-id="f7442-103">Ottiene le impostazioni di controllo di un server SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="f7442-103">Gets the auditing settings of an Azure SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f7442-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f7442-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerAuditing [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7442-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f7442-105">DESCRIPTION</span></span>
<span data-ttu-id="f7442-106">Il cmdlet **Get-AzureRmSqlServerAuditing** ottiene i criteri di controllo BLOB di un server SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="f7442-106">The **Get-AzureRmSqlServerAuditing** cmdlet gets the blob auditing policy of an Azure SQL server.</span></span>
<span data-ttu-id="f7442-107">Specificare i parametri *ResourceGroupName* e *ServerName* per identificare il database.</span><span class="sxs-lookup"><span data-stu-id="f7442-107">Specify the *ResourceGroupName* and *ServerName* parameters to identify the database.</span></span>
<span data-ttu-id="f7442-108">Questo cmdlet restituisce un criterio usato dai database SQL di Azure definiti nell'Azure SQL Server specificato.</span><span class="sxs-lookup"><span data-stu-id="f7442-108">This cmdlet returns a policy that is used by the Azure SQL databases that are defined in the specified Azure SQL server.</span></span>

## <span data-ttu-id="f7442-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f7442-109">EXAMPLES</span></span>

### <span data-ttu-id="f7442-110">Esempio 1: recuperare le impostazioni di controllo di un server SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="f7442-110">Example 1: Get the auditing settings of an Azure SQL server</span></span>
```
PS C:\>Get-AzureRmSqlServerAuditing -ResourceGroupName "resourcegroup01" -ServerName "server01"
AuditActionGroup       : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                          BATCH_COMPLETED_GROUP, ...}
ResourceGroupName      : resourcegroup01
ServerName             : server01
AuditState             : Enabled
StorageAccountName     : mystorage
StorageKeyType         : Primary
RetentionInDays        : 0
```

## <span data-ttu-id="f7442-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f7442-111">PARAMETERS</span></span>

### <span data-ttu-id="f7442-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7442-112">-DefaultProfile</span></span>
<span data-ttu-id="f7442-113">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="f7442-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7442-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7442-114">-ResourceGroupName</span></span>
<span data-ttu-id="f7442-115">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f7442-115">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7442-116">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="f7442-116">-ServerName</span></span>
<span data-ttu-id="f7442-117">Nome di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="f7442-117">SQL server name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7442-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f7442-118">-Confirm</span></span>
<span data-ttu-id="f7442-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7442-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7442-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7442-120">-WhatIf</span></span>
<span data-ttu-id="f7442-121">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f7442-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f7442-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f7442-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7442-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7442-123">CommonParameters</span></span>
<span data-ttu-id="f7442-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7442-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7442-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7442-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7442-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f7442-126">INPUTS</span></span>

### <span data-ttu-id="f7442-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f7442-127">None</span></span>
<span data-ttu-id="f7442-128">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="f7442-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f7442-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f7442-129">OUTPUTS</span></span>

### <span data-ttu-id="f7442-130">Microsoft. Azure. Commands. SQL. Security. Model. ServerBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="f7442-130">Microsoft.Azure.Commands.Sql.Security.Model.ServerBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="f7442-131">Note</span><span class="sxs-lookup"><span data-stu-id="f7442-131">NOTES</span></span>

## <span data-ttu-id="f7442-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f7442-132">RELATED LINKS</span></span>
