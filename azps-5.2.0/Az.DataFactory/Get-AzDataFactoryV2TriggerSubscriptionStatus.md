---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2triggersubscriptionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2TriggerSubscriptionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2TriggerSubscriptionStatus.md
ms.openlocfilehash: 62418f0840e2bbeef016d53c3136f155c4de055f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98363128"
---
# <span data-ttu-id="bf1be-101">Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="bf1be-101">Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>

## <span data-ttu-id="bf1be-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bf1be-102">SYNOPSIS</span></span>
<span data-ttu-id="bf1be-103">Ottenere lo stato della sottoscrizione per il trigger dell'evento per gli eventi del servizio esterno specificati.</span><span class="sxs-lookup"><span data-stu-id="bf1be-103">Get the status of the subscription for the event trigger to the specified external service events.</span></span>

## <span data-ttu-id="bf1be-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bf1be-104">SYNTAX</span></span>

### <span data-ttu-id="bf1be-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="bf1be-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2TriggerSubscriptionStatus [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bf1be-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="bf1be-106">ByInputObject</span></span>
```
Get-AzDataFactoryV2TriggerSubscriptionStatus [-InputObject] <PSTrigger>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bf1be-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="bf1be-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2TriggerSubscriptionStatus [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bf1be-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bf1be-108">DESCRIPTION</span></span>
<span data-ttu-id="bf1be-109">Questo comando ottiene lo stato della sottoscrizione per il trigger dell'evento per gli eventi del servizio esterno specificati.</span><span class="sxs-lookup"><span data-stu-id="bf1be-109">This command gets the status of the subscription for the event trigger to the specified external service events.</span></span> <span data-ttu-id="bf1be-110">Il trigger non può essere avviato finché lo stato restituito non è "Enabled".</span><span class="sxs-lookup"><span data-stu-id="bf1be-110">The trigger can't be started until the returned status is "Enabled".</span></span>

## <span data-ttu-id="bf1be-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bf1be-111">EXAMPLES</span></span>

### <span data-ttu-id="bf1be-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="bf1be-112">Example 1</span></span>
```
PS C:\> Get-AzDataFactoryV2TriggerSubscriptionStatus -ResourceGroupName ADF -DataFactoryName WikiADF -Name Trigger1

TriggerName Status
----------- ------
Trigger1    Enabled
```

<span data-ttu-id="bf1be-113">Questo comando otterrà lo stato del trigger abbonamento for BlobEnetTrigger1 per gli eventi del servizio esterno.</span><span class="sxs-lookup"><span data-stu-id="bf1be-113">This command will get the status of the subscribtion for BlobEnetTrigger1 trigger to the external service events.</span></span>

## <span data-ttu-id="bf1be-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bf1be-114">PARAMETERS</span></span>

### <span data-ttu-id="bf1be-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="bf1be-115">-DataFactoryName</span></span>
<span data-ttu-id="bf1be-116">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="bf1be-116">The data factory name.</span></span>

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

### <span data-ttu-id="bf1be-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf1be-117">-DefaultProfile</span></span>
<span data-ttu-id="bf1be-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bf1be-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf1be-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bf1be-119">-InputObject</span></span>
<span data-ttu-id="bf1be-120">Oggetto trigger.</span><span class="sxs-lookup"><span data-stu-id="bf1be-120">The trigger object.</span></span>

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

### <span data-ttu-id="bf1be-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="bf1be-121">-Name</span></span>
<span data-ttu-id="bf1be-122">Nome del trigger.</span><span class="sxs-lookup"><span data-stu-id="bf1be-122">The trigger name.</span></span>

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

### <span data-ttu-id="bf1be-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf1be-123">-ResourceGroupName</span></span>
<span data-ttu-id="bf1be-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="bf1be-124">The resource group name.</span></span>

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

### <span data-ttu-id="bf1be-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bf1be-125">-ResourceId</span></span>
<span data-ttu-id="bf1be-126">ID risorsa di Azure.</span><span class="sxs-lookup"><span data-stu-id="bf1be-126">The Azure resource ID.</span></span>

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

### <span data-ttu-id="bf1be-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf1be-127">CommonParameters</span></span>
<span data-ttu-id="bf1be-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf1be-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf1be-129">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf1be-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf1be-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bf1be-130">INPUTS</span></span>

### <span data-ttu-id="bf1be-131">System. String</span><span class="sxs-lookup"><span data-stu-id="bf1be-131">System.String</span></span>
<span data-ttu-id="bf1be-132">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="bf1be-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="bf1be-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bf1be-133">OUTPUTS</span></span>

### <span data-ttu-id="bf1be-134">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="bf1be-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="bf1be-135">Note</span><span class="sxs-lookup"><span data-stu-id="bf1be-135">NOTES</span></span>

## <span data-ttu-id="bf1be-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bf1be-136">RELATED LINKS</span></span>

