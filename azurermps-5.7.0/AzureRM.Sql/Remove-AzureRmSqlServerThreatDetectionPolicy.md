---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: DCAB75A1-B4EF-4C41-9D6B-A954B6DB0028
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlserverthreatdetectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerThreatDetectionPolicy.md
ms.openlocfilehash: d9763bf02054962eac955188860e97ed271d7a7c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512207"
---
# <span data-ttu-id="4a28d-101">Remove-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="4a28d-101">Remove-AzureRmSqlServerThreatDetectionPolicy</span></span>

## <span data-ttu-id="4a28d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4a28d-102">SYNOPSIS</span></span>
<span data-ttu-id="4a28d-103">Rimuove i criteri di rilevamento delle minacce da un server.</span><span class="sxs-lookup"><span data-stu-id="4a28d-103">Removes the threat detection policy from a server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4a28d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4a28d-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerThreatDetectionPolicy [-PassThru] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a28d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4a28d-105">DESCRIPTION</span></span>
<span data-ttu-id="4a28d-106">Il cmdlet Remove-AzureRmSqlServerThreatDetectionPolicy rimuove i criteri di rilevamento delle minacce da un server SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="4a28d-106">The Remove-AzureRmSqlServerThreatDetectionPolicy cmdlet removes the threat detection policy from an Azure SQL server.</span></span>

<span data-ttu-id="4a28d-107">Per usare questo cmdlet, specificare i parametri ResourceGroupName e ServerName per identificare il server da cui questo cmdlet rimuove il criterio.</span><span class="sxs-lookup"><span data-stu-id="4a28d-107">To use this cmdlet, specify the ResourceGroupName and ServerName parameters to identify the server from which this cmdlet removes the policy.</span></span>

## <span data-ttu-id="4a28d-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4a28d-108">EXAMPLES</span></span>

### <span data-ttu-id="4a28d-109">Esempio 1: rimuovere un criterio di rilevamento delle minacce per un database</span><span class="sxs-lookup"><span data-stu-id="4a28d-109">Example 1: Remove a threat detection policy for a database</span></span>
```
PS C:\> Remove-AzureRmSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

<span data-ttu-id="4a28d-110">Questo comando rimuove i criteri di rilevamento delle minacce da un server denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="4a28d-110">This command removes the threat detection policy from a server named Server01.</span></span>

## <span data-ttu-id="4a28d-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4a28d-111">PARAMETERS</span></span>

### <span data-ttu-id="4a28d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a28d-112">-DefaultProfile</span></span>
<span data-ttu-id="4a28d-113">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="4a28d-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4a28d-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4a28d-114">-PassThru</span></span>
<span data-ttu-id="4a28d-115">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="4a28d-115">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="4a28d-116">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="4a28d-116">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a28d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a28d-117">-ResourceGroupName</span></span>
<span data-ttu-id="4a28d-118">Specifica il nome del gruppo di risorse a cui è assegnato il server.</span><span class="sxs-lookup"><span data-stu-id="4a28d-118">Specifies the name of the resource group the server is assigned to.</span></span>

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

### <span data-ttu-id="4a28d-119">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="4a28d-119">-ServerName</span></span>
<span data-ttu-id="4a28d-120">Specifica il nome di un server.</span><span class="sxs-lookup"><span data-stu-id="4a28d-120">Specifies the name of a server.</span></span>

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

### <span data-ttu-id="4a28d-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4a28d-121">-Confirm</span></span>
<span data-ttu-id="4a28d-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4a28d-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a28d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a28d-123">-WhatIf</span></span>
<span data-ttu-id="4a28d-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4a28d-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a28d-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4a28d-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a28d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a28d-126">CommonParameters</span></span>
<span data-ttu-id="4a28d-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a28d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a28d-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a28d-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a28d-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4a28d-129">INPUTS</span></span>

###  
<span data-ttu-id="4a28d-130">Non è possibile reindirizzare l'input a questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4a28d-130">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="4a28d-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4a28d-131">OUTPUTS</span></span>

### <span data-ttu-id="4a28d-132">Microsoft. Azure. Commands. SQL. ThreatDetection. Model. ServerThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="4a28d-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionPolicyModel</span></span>
<span data-ttu-id="4a28d-133">Questo cmdlet restituisce un oggetto ServerThreatDetectionPolicyModel.</span><span class="sxs-lookup"><span data-stu-id="4a28d-133">This cmdlet returns a ServerThreatDetectionPolicyModel object.</span></span>

## <span data-ttu-id="4a28d-134">Note</span><span class="sxs-lookup"><span data-stu-id="4a28d-134">NOTES</span></span>

## <span data-ttu-id="4a28d-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4a28d-135">RELATED LINKS</span></span>

[<span data-ttu-id="4a28d-136">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="4a28d-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

