---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2triggersubscriptionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2TriggerSubscriptionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2TriggerSubscriptionStatus.md
ms.openlocfilehash: 62418f0840e2bbeef016d53c3136f155c4de055f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196598"
---
# <span data-ttu-id="b2ca7-101">Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="b2ca7-101">Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>

## <span data-ttu-id="b2ca7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2ca7-102">SYNOPSIS</span></span>
<span data-ttu-id="b2ca7-103">Ottenere lo stato della sottoscrizione per il trigger di evento per gli eventi del servizio esterno specificati.</span><span class="sxs-lookup"><span data-stu-id="b2ca7-103">Get the status of the subscription for the event trigger to the specified external service events.</span></span>

## <span data-ttu-id="b2ca7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b2ca7-104">SYNTAX</span></span>

### <span data-ttu-id="b2ca7-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="b2ca7-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2TriggerSubscriptionStatus [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2ca7-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="b2ca7-106">ByInputObject</span></span>
```
Get-AzDataFactoryV2TriggerSubscriptionStatus [-InputObject] <PSTrigger>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2ca7-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b2ca7-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2TriggerSubscriptionStatus [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b2ca7-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b2ca7-108">DESCRIPTION</span></span>
<span data-ttu-id="b2ca7-109">Questo comando recupera lo stato della sottoscrizione per il trigger di evento per gli eventi del servizio esterno specificati.</span><span class="sxs-lookup"><span data-stu-id="b2ca7-109">This command gets the status of the subscription for the event trigger to the specified external service events.</span></span> <span data-ttu-id="b2ca7-110">Il trigger non può essere avviato finché lo stato restituito non è "Abilitato".</span><span class="sxs-lookup"><span data-stu-id="b2ca7-110">The trigger can't be started until the returned status is "Enabled".</span></span>

## <span data-ttu-id="b2ca7-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b2ca7-111">EXAMPLES</span></span>

### <span data-ttu-id="b2ca7-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b2ca7-112">Example 1</span></span>
```
PS C:\> Get-AzDataFactoryV2TriggerSubscriptionStatus -ResourceGroupName ADF -DataFactoryName WikiADF -Name Trigger1

TriggerName Status
----------- ------
Trigger1    Enabled
```

<span data-ttu-id="b2ca7-113">Questo comando ottiene lo stato dell'attivazione di BLOBEnetTrigger1 per gli eventi del servizio esterno.</span><span class="sxs-lookup"><span data-stu-id="b2ca7-113">This command will get the status of the subscribtion for BlobEnetTrigger1 trigger to the external service events.</span></span>

## <span data-ttu-id="b2ca7-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b2ca7-114">PARAMETERS</span></span>

### <span data-ttu-id="b2ca7-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="b2ca7-115">-DataFactoryName</span></span>
<span data-ttu-id="b2ca7-116">Nome del data factory.</span><span class="sxs-lookup"><span data-stu-id="b2ca7-116">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2ca7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2ca7-117">-DefaultProfile</span></span>
<span data-ttu-id="b2ca7-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b2ca7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2ca7-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b2ca7-119">-InputObject</span></span>
<span data-ttu-id="b2ca7-120">Oggetto trigger.</span><span class="sxs-lookup"><span data-stu-id="b2ca7-120">The trigger object.</span></span>

```yaml
Type: PSTrigger
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b2ca7-121">-Name</span><span class="sxs-lookup"><span data-stu-id="b2ca7-121">-Name</span></span>
<span data-ttu-id="b2ca7-122">Nome del trigger.</span><span class="sxs-lookup"><span data-stu-id="b2ca7-122">The trigger name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2ca7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2ca7-123">-ResourceGroupName</span></span>
<span data-ttu-id="b2ca7-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b2ca7-124">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2ca7-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b2ca7-125">-ResourceId</span></span>
<span data-ttu-id="b2ca7-126">ID della risorsa Azure.</span><span class="sxs-lookup"><span data-stu-id="b2ca7-126">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2ca7-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2ca7-127">CommonParameters</span></span>
<span data-ttu-id="b2ca7-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2ca7-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2ca7-129">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2ca7-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2ca7-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="b2ca7-130">INPUTS</span></span>

### <span data-ttu-id="b2ca7-131">System.String</span><span class="sxs-lookup"><span data-stu-id="b2ca7-131">System.String</span></span>
<span data-ttu-id="b2ca7-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span><span class="sxs-lookup"><span data-stu-id="b2ca7-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="b2ca7-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b2ca7-133">OUTPUTS</span></span>

### <span data-ttu-id="b2ca7-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="b2ca7-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="b2ca7-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="b2ca7-135">NOTES</span></span>

## <span data-ttu-id="b2ca7-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b2ca7-136">RELATED LINKS</span></span>

