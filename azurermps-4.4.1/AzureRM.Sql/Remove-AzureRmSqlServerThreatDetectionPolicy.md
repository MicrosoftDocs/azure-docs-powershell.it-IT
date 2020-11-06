---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: DCAB75A1-B4EF-4C41-9D6B-A954B6DB0028
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerThreatDetectionPolicy.md
ms.openlocfilehash: e6a47578ef2442e6ca2f6d03284624f1f2906e35
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511231"
---
# <span data-ttu-id="84b6b-101">Remove-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="84b6b-101">Remove-AzureRmSqlServerThreatDetectionPolicy</span></span>

## <span data-ttu-id="84b6b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="84b6b-102">SYNOPSIS</span></span>
<span data-ttu-id="84b6b-103">Rimuove i criteri di rilevamento delle minacce da un server.</span><span class="sxs-lookup"><span data-stu-id="84b6b-103">Removes the threat detection policy from a server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="84b6b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="84b6b-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerThreatDetectionPolicy [-PassThru] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84b6b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="84b6b-105">DESCRIPTION</span></span>
<span data-ttu-id="84b6b-106">Il cmdlet Remove-AzureRmSqlServerThreatDetectionPolicy rimuove i criteri di rilevamento delle minacce da un server SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="84b6b-106">The Remove-AzureRmSqlServerThreatDetectionPolicy cmdlet removes the threat detection policy from an Azure SQL server.</span></span>

<span data-ttu-id="84b6b-107">Per usare questo cmdlet, specificare i parametri ResourceGroupName e ServerName per identificare il server da cui questo cmdlet rimuove il criterio.</span><span class="sxs-lookup"><span data-stu-id="84b6b-107">To use this cmdlet, specify the ResourceGroupName and ServerName parameters to identify the server from which this cmdlet removes the policy.</span></span>

## <span data-ttu-id="84b6b-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="84b6b-108">EXAMPLES</span></span>

### <span data-ttu-id="84b6b-109">--------------------------Esempio 1: rimuovere un criterio di rilevamento delle minacce per un database--------------------------</span><span class="sxs-lookup"><span data-stu-id="84b6b-109">--------------------------  Example 1: Remove a threat detection policy for a database  --------------------------</span></span>
```
PS C:\> Remove-AzureRmSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

<span data-ttu-id="84b6b-110">Questo comando rimuove i criteri di rilevamento delle minacce da un server denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="84b6b-110">This command removes the threat detection policy from a server named Server01.</span></span>

## <span data-ttu-id="84b6b-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="84b6b-111">PARAMETERS</span></span>

### <span data-ttu-id="84b6b-112">-PassThru</span><span class="sxs-lookup"><span data-stu-id="84b6b-112">-PassThru</span></span>
<span data-ttu-id="84b6b-113">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="84b6b-113">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="84b6b-114">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="84b6b-114">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84b6b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84b6b-115">-ResourceGroupName</span></span>
<span data-ttu-id="84b6b-116">Specifica il nome del gruppo di risorse a cui è assegnato il server.</span><span class="sxs-lookup"><span data-stu-id="84b6b-116">Specifies the name of the resource group the server is assigned to.</span></span>

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

### <span data-ttu-id="84b6b-117">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="84b6b-117">-ServerName</span></span>
<span data-ttu-id="84b6b-118">Specifica il nome di un server.</span><span class="sxs-lookup"><span data-stu-id="84b6b-118">Specifies the name of a server.</span></span>

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

### <span data-ttu-id="84b6b-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="84b6b-119">-Confirm</span></span>
<span data-ttu-id="84b6b-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="84b6b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84b6b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84b6b-121">-WhatIf</span></span>
<span data-ttu-id="84b6b-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="84b6b-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84b6b-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="84b6b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84b6b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84b6b-124">-DefaultProfile</span></span>
<span data-ttu-id="84b6b-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="84b6b-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="84b6b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84b6b-126">CommonParameters</span></span>
<span data-ttu-id="84b6b-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84b6b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84b6b-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84b6b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84b6b-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="84b6b-129">INPUTS</span></span>

###  
<span data-ttu-id="84b6b-130">Non è possibile reindirizzare l'input a questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="84b6b-130">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="84b6b-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="84b6b-131">OUTPUTS</span></span>

### <span data-ttu-id="84b6b-132">Microsoft. Azure. Commands. SQL. ThreatDetection. Model. ServerThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="84b6b-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionPolicyModel</span></span>
<span data-ttu-id="84b6b-133">Questo cmdlet restituisce un oggetto ServerThreatDetectionPolicyModel.</span><span class="sxs-lookup"><span data-stu-id="84b6b-133">This cmdlet returns a ServerThreatDetectionPolicyModel object.</span></span>

## <span data-ttu-id="84b6b-134">Note</span><span class="sxs-lookup"><span data-stu-id="84b6b-134">NOTES</span></span>

## <span data-ttu-id="84b6b-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="84b6b-135">RELATED LINKS</span></span>

[<span data-ttu-id="84b6b-136">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="84b6b-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

