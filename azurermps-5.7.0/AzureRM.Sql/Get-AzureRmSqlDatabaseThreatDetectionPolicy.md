---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 017EF522-ABC5-40EE-B8DC-369D097F49D0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabasethreatdetectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseThreatDetectionPolicy.md
ms.openlocfilehash: ad07f080b659ff03c96f806ad7b69446c4491fb7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517924"
---
# <span data-ttu-id="19922-101">Get-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="19922-101">Get-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>

## <span data-ttu-id="19922-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="19922-102">SYNOPSIS</span></span>
<span data-ttu-id="19922-103">Ottiene i criteri di rilevamento delle minacce per un database.</span><span class="sxs-lookup"><span data-stu-id="19922-103">Gets the threat detection policy for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="19922-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="19922-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseThreatDetectionPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="19922-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="19922-105">DESCRIPTION</span></span>
<span data-ttu-id="19922-106">Il cmdlet **Get-AzureRmSqlDatabaseThreatDetectionPolicy** ottiene i criteri di rilevamento delle minacce di un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="19922-106">The **Get-AzureRmSqlDatabaseThreatDetectionPolicy** cmdlet gets the threat detection policy of an Azure SQL database.</span></span>
<span data-ttu-id="19922-107">Per usare questo cmdlet, specificare i parametri *ResourceGroupName* , *ServerName* e *DatabaseName* per identificare il database per cui questo cmdlet ottiene i criteri.</span><span class="sxs-lookup"><span data-stu-id="19922-107">To use this cmdlet, specify the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database for which this cmdlet gets the policy.</span></span>

## <span data-ttu-id="19922-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="19922-108">EXAMPLES</span></span>

### <span data-ttu-id="19922-109">Esempio 1: ottenere i criteri di rilevamento delle minacce per un database</span><span class="sxs-lookup"><span data-stu-id="19922-109">Example 1: Get the threat detection policy for a database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName                 : Database01
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

<span data-ttu-id="19922-110">Questo comando consente di ottenere i criteri di rilevamento delle minacce per un database denominato Database01.</span><span class="sxs-lookup"><span data-stu-id="19922-110">This command gets the threat detection policy for a database named Database01.</span></span>
<span data-ttu-id="19922-111">Il database si trova nel server denominato Server01, assegnato al gruppo di risorse ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="19922-111">The database is located on the server named Server01, which is assigned to the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="19922-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="19922-112">PARAMETERS</span></span>

### <span data-ttu-id="19922-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="19922-113">-DatabaseName</span></span>
<span data-ttu-id="19922-114">Specifica il nome di un database.</span><span class="sxs-lookup"><span data-stu-id="19922-114">Specifies the name of a database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19922-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19922-115">-DefaultProfile</span></span>
<span data-ttu-id="19922-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="19922-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="19922-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19922-117">-ResourceGroupName</span></span>
<span data-ttu-id="19922-118">Specifica il nome del gruppo di risorse a cui è assegnato il server.</span><span class="sxs-lookup"><span data-stu-id="19922-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="19922-119">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="19922-119">-ServerName</span></span>
<span data-ttu-id="19922-120">Specifica il nome di un server.</span><span class="sxs-lookup"><span data-stu-id="19922-120">Specifies the name of a server.</span></span>

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

### <span data-ttu-id="19922-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="19922-121">-Confirm</span></span>
<span data-ttu-id="19922-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19922-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19922-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19922-123">-WhatIf</span></span>
<span data-ttu-id="19922-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="19922-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19922-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="19922-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19922-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19922-126">CommonParameters</span></span>
<span data-ttu-id="19922-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19922-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19922-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19922-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19922-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="19922-129">INPUTS</span></span>

###  
<span data-ttu-id="19922-130">Non è possibile reindirizzare l'input a questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19922-130">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="19922-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="19922-131">OUTPUTS</span></span>

### <span data-ttu-id="19922-132">Microsoft. Azure. Commands. SQL. ThreatDetection. Model. DatabaseThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="19922-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionPolicyModel</span></span>
<span data-ttu-id="19922-133">Questo cmdlet restituisce un oggetto **Model. DatabaseThreatDetectionPolicyModel** .</span><span class="sxs-lookup"><span data-stu-id="19922-133">This cmdlet returns a **Model.DatabaseThreatDetectionPolicyModel** object.</span></span>

## <span data-ttu-id="19922-134">Note</span><span class="sxs-lookup"><span data-stu-id="19922-134">NOTES</span></span>

## <span data-ttu-id="19922-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="19922-135">RELATED LINKS</span></span>

[<span data-ttu-id="19922-136">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="19922-136">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>](./Remove-AzureRmSqlDatabaseThreatDetectionPolicy.md)


