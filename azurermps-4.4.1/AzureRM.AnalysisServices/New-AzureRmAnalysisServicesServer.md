---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: 0093393f926af257e07b7d697a7f267fa62b483a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508859"
---
# <span data-ttu-id="9f744-101">New-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="9f744-101">New-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="9f744-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9f744-102">SYNOPSIS</span></span>
<span data-ttu-id="9f744-103">Crea un nuovo server di Analysis Services</span><span class="sxs-lookup"><span data-stu-id="9f744-103">Creates a new Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9f744-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9f744-104">SYNTAX</span></span>

```
New-AzureRmAnalysisServicesServer [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Sku] <String> [[-Tag] <Hashtable>] [[-Administrator] <String>] [[-BackupBlobContainerUri] <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f744-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9f744-105">DESCRIPTION</span></span>
<span data-ttu-id="9f744-106">Il cmdlet New-AzureRmAnalysisServicesServer crea un nuovo server di Analysis Services</span><span class="sxs-lookup"><span data-stu-id="9f744-106">The New-AzureRmAnalysisServicesServer cmdlet creates a new Analysis Services server</span></span>

## <span data-ttu-id="9f744-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9f744-107">EXAMPLES</span></span>

### <span data-ttu-id="9f744-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9f744-108">Example 1</span></span>
```
PS C:\> New-AzureRmAnalysisServicesServer -ResourceGroupName "testresourcegroup" -Name "testserver" -Location "West-US" -Sku "S1"
```

<span data-ttu-id="9f744-109">Crea un server denominato TestServer in Azure Region West-US e nel gruppo di risorse testresrourcegroup.</span><span class="sxs-lookup"><span data-stu-id="9f744-109">Creates a server named testserver in the Azure region West-US and in resource group testresrourcegroup.</span></span> <span data-ttu-id="9f744-110">Il livello SKU per il server sarà S1.</span><span class="sxs-lookup"><span data-stu-id="9f744-110">The sku level for the server will be S1.</span></span>

## <span data-ttu-id="9f744-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9f744-111">PARAMETERS</span></span>

### <span data-ttu-id="9f744-112">-Amministratore</span><span class="sxs-lookup"><span data-stu-id="9f744-112">-Administrator</span></span>
<span data-ttu-id="9f744-113">Stringa che rappresenta un elenco delimitato da virgole di utenti o gruppi da impostare come amministratori nel server.</span><span class="sxs-lookup"><span data-stu-id="9f744-113">A string representing a comma separated list of users or groups to be set as administrators on the server.</span></span> <span data-ttu-id="9f744-114">Gli utenti o i gruppi devono essere specificati come formato user@contoso.com UPN, ad esempio groups@contoso.com</span><span class="sxs-lookup"><span data-stu-id="9f744-114">The users or groups need to be specified UPN format e.g. user@contoso.com or groups@contoso.com</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f744-115">-BackupBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="9f744-115">-BackupBlobContainerUri</span></span>
<span data-ttu-id="9f744-116">URI del contenitore BLOB per il backup del server di Analysis Services</span><span class="sxs-lookup"><span data-stu-id="9f744-116">The blob container Uri for backup the Analysis Services server</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f744-117">-Posizione</span><span class="sxs-lookup"><span data-stu-id="9f744-117">-Location</span></span>
<span data-ttu-id="9f744-118">Area di Azure in cui è ospitato il server Analysis Services</span><span class="sxs-lookup"><span data-stu-id="9f744-118">The Azure region where the Analysis Services server is hosted</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: North Central US, South Central US, Central US, West Europe, North Europe, West US, East US, East US 2, Japan East, Japan West, Brazil South, Southeast Asia, East Asia, Australia East, Australia Southeast

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f744-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="9f744-119">-Name</span></span>
<span data-ttu-id="9f744-120">Nome del server di Analysis Services</span><span class="sxs-lookup"><span data-stu-id="9f744-120">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="9f744-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f744-121">-ResourceGroupName</span></span>
<span data-ttu-id="9f744-122">Nome del gruppo di risorse Azure a cui appartiene il server</span><span class="sxs-lookup"><span data-stu-id="9f744-122">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="9f744-123">-SKU</span><span class="sxs-lookup"><span data-stu-id="9f744-123">-Sku</span></span>
<span data-ttu-id="9f744-124">Nome dell'USK per il server.</span><span class="sxs-lookup"><span data-stu-id="9f744-124">The name of the Sku for the server.</span></span>
<span data-ttu-id="9f744-125">I valori supportati sono 0',' s 1',' s 2',' s 4' per il livello standard; ' B1',' B2' per il livello di base è da 1' per il livello di sviluppo.</span><span class="sxs-lookup"><span data-stu-id="9f744-125">The supported values are 'S0', 'S1', 'S2', 'S4' for the Standard tier; 'B1', 'B2' for the Basic tier and 'D1' for Development tier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f744-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="9f744-126">-Tag</span></span>
<span data-ttu-id="9f744-127">Coppie chiave-valore nella forma di una tabella hash impostata come tag nel server.</span><span class="sxs-lookup"><span data-stu-id="9f744-127">Key-value pairs in the form of a hash table set as tags on the server.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f744-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9f744-128">-Confirm</span></span>
<span data-ttu-id="9f744-129">Chiede all'utente di confermare se eseguire l'operazione</span><span class="sxs-lookup"><span data-stu-id="9f744-129">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="9f744-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f744-130">-WhatIf</span></span>
<span data-ttu-id="9f744-131">Descrive le azioni che verranno eseguite dall'operazione corrente senza eseguirle effettivamente</span><span class="sxs-lookup"><span data-stu-id="9f744-131">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="9f744-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f744-132">CommonParameters</span></span>
<span data-ttu-id="9f744-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f744-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f744-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f744-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f744-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9f744-135">INPUTS</span></span>

## <span data-ttu-id="9f744-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9f744-136">OUTPUTS</span></span>

### <span data-ttu-id="9f744-137">Microsoft. Azure. Commands. AnalysisServices. Models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="9f744-137">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="9f744-138">Note</span><span class="sxs-lookup"><span data-stu-id="9f744-138">NOTES</span></span>
<span data-ttu-id="9f744-139">Alias: New-AzureAs</span><span class="sxs-lookup"><span data-stu-id="9f744-139">Alias: New-AzureAs</span></span>

## <span data-ttu-id="9f744-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9f744-140">RELATED LINKS</span></span>

[<span data-ttu-id="9f744-141">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="9f744-141">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="9f744-142">Remove-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="9f744-142">Remove-AzureRmAnalysisServicesServer</span></span>](./Remove-AzureRmAnalysisServicesServer.md)
