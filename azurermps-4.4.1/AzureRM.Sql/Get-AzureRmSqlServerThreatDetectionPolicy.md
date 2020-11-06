---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: F26CB715-D66A-4672-AA47-F3B316957FC8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerThreatDetectionPolicy.md
ms.openlocfilehash: 1cb77a435ee951e2e7fe4bc7401e7e4385557eaa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519954"
---
# <span data-ttu-id="1d1f7-101">Get-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="1d1f7-101">Get-AzureRmSqlServerThreatDetectionPolicy</span></span>

## <span data-ttu-id="1d1f7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1d1f7-102">SYNOPSIS</span></span>
<span data-ttu-id="1d1f7-103">Ottiene i criteri di rilevamento delle minacce per un server.</span><span class="sxs-lookup"><span data-stu-id="1d1f7-103">Gets the threat detection policy for a server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1d1f7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1d1f7-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerThreatDetectionPolicy -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d1f7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1d1f7-105">DESCRIPTION</span></span>
<span data-ttu-id="1d1f7-106">Il cmdlet **Get-AzureRmSqlServerThreatDetectionPolicy** ottiene i criteri di rilevamento delle minacce di un server SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="1d1f7-106">The **Get-AzureRmSqlServerThreatDetectionPolicy** cmdlet gets the threat detection policy of an Azure SQL server.</span></span>
<span data-ttu-id="1d1f7-107">Per usare questo cmdlet, specificare i parametri *ResourceGroupName* e *ServerName* per identificare il server per cui questo cmdlet ottiene i criteri.</span><span class="sxs-lookup"><span data-stu-id="1d1f7-107">To use this cmdlet, specify the *ResourceGroupName* and *ServerName* parameters to identify the server for which this cmdlet gets the policy.</span></span>

## <span data-ttu-id="1d1f7-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1d1f7-108">EXAMPLES</span></span>

### <span data-ttu-id="1d1f7-109">Esempio 1: ottenere i criteri di rilevamento delle minacce per un server</span><span class="sxs-lookup"><span data-stu-id="1d1f7-109">Example 1: Get the threat detection policy for a server</span></span>
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

<span data-ttu-id="1d1f7-110">Questo comando ottiene i criteri di rilevamento delle minacce per un server denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="1d1f7-110">This command gets the threat detection policy for a server named Server01.</span></span>
<span data-ttu-id="1d1f7-111">Il server viene assegnato al gruppo di risorse ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="1d1f7-111">The server is assigned to the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="1d1f7-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1d1f7-112">PARAMETERS</span></span>

### <span data-ttu-id="1d1f7-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d1f7-113">-ResourceGroupName</span></span>
<span data-ttu-id="1d1f7-114">Specifica il nome del gruppo di risorse a cui appartiene il server.</span><span class="sxs-lookup"><span data-stu-id="1d1f7-114">Specifies the name of the resource group to which the server belongs.</span></span>

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

### <span data-ttu-id="1d1f7-115">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="1d1f7-115">-ServerName</span></span>
<span data-ttu-id="1d1f7-116">Specifica il nome del server.</span><span class="sxs-lookup"><span data-stu-id="1d1f7-116">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="1d1f7-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1d1f7-117">-Confirm</span></span>
<span data-ttu-id="1d1f7-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d1f7-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d1f7-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d1f7-119">-WhatIf</span></span>
<span data-ttu-id="1d1f7-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1d1f7-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d1f7-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1d1f7-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d1f7-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d1f7-122">-DefaultProfile</span></span>
<span data-ttu-id="1d1f7-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1d1f7-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d1f7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d1f7-124">CommonParameters</span></span>
<span data-ttu-id="1d1f7-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d1f7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d1f7-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d1f7-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d1f7-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1d1f7-127">INPUTS</span></span>

## <span data-ttu-id="1d1f7-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1d1f7-128">OUTPUTS</span></span>

### <span data-ttu-id="1d1f7-129">Microsoft. Azure. Commands. SQL. ThreatDetection. Model. ServerThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="1d1f7-129">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionPolicyModel</span></span>

## <span data-ttu-id="1d1f7-130">Note</span><span class="sxs-lookup"><span data-stu-id="1d1f7-130">NOTES</span></span>

## <span data-ttu-id="1d1f7-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1d1f7-131">RELATED LINKS</span></span>

[<span data-ttu-id="1d1f7-132">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="1d1f7-132">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>](./Remove-AzureRmSqlDatabaseThreatDetectionPolicy.md)

[<span data-ttu-id="1d1f7-133">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="1d1f7-133">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


