---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: F26CB715-D66A-4672-AA47-F3B316957FC8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverthreatdetectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerThreatDetectionPolicy.md
ms.openlocfilehash: 5ee1039f938c561424ded9768e9d5f84372410fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507860"
---
# <span data-ttu-id="a155c-101">Get-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="a155c-101">Get-AzureRmSqlServerThreatDetectionPolicy</span></span>

## <span data-ttu-id="a155c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a155c-102">SYNOPSIS</span></span>
<span data-ttu-id="a155c-103">Ottiene i criteri di rilevamento delle minacce per un server.</span><span class="sxs-lookup"><span data-stu-id="a155c-103">Gets the threat detection policy for a server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a155c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a155c-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerThreatDetectionPolicy -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a155c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a155c-105">DESCRIPTION</span></span>
<span data-ttu-id="a155c-106">Il cmdlet **Get-AzureRmSqlServerThreatDetectionPolicy** ottiene i criteri di rilevamento delle minacce di un server SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="a155c-106">The **Get-AzureRmSqlServerThreatDetectionPolicy** cmdlet gets the threat detection policy of an Azure SQL server.</span></span>
<span data-ttu-id="a155c-107">Per usare questo cmdlet, specificare i parametri *ResourceGroupName* e *ServerName* per identificare il server per cui questo cmdlet ottiene i criteri.</span><span class="sxs-lookup"><span data-stu-id="a155c-107">To use this cmdlet, specify the *ResourceGroupName* and *ServerName* parameters to identify the server for which this cmdlet gets the policy.</span></span>

## <span data-ttu-id="a155c-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a155c-108">EXAMPLES</span></span>

### <span data-ttu-id="a155c-109">Esempio 1: ottenere i criteri di rilevamento delle minacce per un server</span><span class="sxs-lookup"><span data-stu-id="a155c-109">Example 1: Get the threat detection policy for a server</span></span>
```
PS C:\>Get-AzureRmSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

<span data-ttu-id="a155c-110">Questo comando ottiene i criteri di rilevamento delle minacce per un server denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="a155c-110">This command gets the threat detection policy for a server named Server01.</span></span>
<span data-ttu-id="a155c-111">Il server viene assegnato al gruppo di risorse ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="a155c-111">The server is assigned to the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="a155c-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a155c-112">PARAMETERS</span></span>

### <span data-ttu-id="a155c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a155c-113">-DefaultProfile</span></span>
<span data-ttu-id="a155c-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="a155c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a155c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a155c-115">-ResourceGroupName</span></span>
<span data-ttu-id="a155c-116">Specifica il nome del gruppo di risorse a cui appartiene il server.</span><span class="sxs-lookup"><span data-stu-id="a155c-116">Specifies the name of the resource group to which the server belongs.</span></span>

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

### <span data-ttu-id="a155c-117">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="a155c-117">-ServerName</span></span>
<span data-ttu-id="a155c-118">Specifica il nome del server.</span><span class="sxs-lookup"><span data-stu-id="a155c-118">Specifies the name of the server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a155c-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a155c-119">-Confirm</span></span>
<span data-ttu-id="a155c-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a155c-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a155c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a155c-121">-WhatIf</span></span>
<span data-ttu-id="a155c-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a155c-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a155c-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a155c-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a155c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a155c-124">CommonParameters</span></span>
<span data-ttu-id="a155c-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a155c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a155c-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a155c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a155c-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a155c-127">INPUTS</span></span>

### <span data-ttu-id="a155c-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a155c-128">None</span></span>
<span data-ttu-id="a155c-129">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="a155c-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a155c-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a155c-130">OUTPUTS</span></span>

### <span data-ttu-id="a155c-131">Microsoft. Azure. Commands. SQL. ThreatDetection. Model. ServerThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="a155c-131">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionPolicyModel</span></span>

## <span data-ttu-id="a155c-132">Note</span><span class="sxs-lookup"><span data-stu-id="a155c-132">NOTES</span></span>

## <span data-ttu-id="a155c-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a155c-133">RELATED LINKS</span></span>

[<span data-ttu-id="a155c-134">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="a155c-134">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>](./Remove-AzureRmSqlDatabaseThreatDetectionPolicy.md)

[<span data-ttu-id="a155c-135">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="a155c-135">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


