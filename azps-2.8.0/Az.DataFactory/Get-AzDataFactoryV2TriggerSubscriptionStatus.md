---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2triggersubscriptionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2TriggerSubscriptionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2TriggerSubscriptionStatus.md
ms.openlocfilehash: fedb3db8ae8d7cd64ab4309da65f9dea998826e4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675001"
---
# <span data-ttu-id="683e2-101">Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="683e2-101">Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>

## <span data-ttu-id="683e2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="683e2-102">SYNOPSIS</span></span>
<span data-ttu-id="683e2-103">Ottenere lo stato della sottoscrizione per il trigger dell'evento per gli eventi del servizio esterno specificati.</span><span class="sxs-lookup"><span data-stu-id="683e2-103">Get the status of the subscription for the event trigger to the specified external service events.</span></span>

## <span data-ttu-id="683e2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="683e2-104">SYNTAX</span></span>

### <span data-ttu-id="683e2-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="683e2-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2TriggerSubscriptionStatus [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="683e2-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="683e2-106">ByInputObject</span></span>
```
Get-AzDataFactoryV2TriggerSubscriptionStatus [-InputObject] <PSTrigger>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="683e2-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="683e2-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2TriggerSubscriptionStatus [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="683e2-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="683e2-108">DESCRIPTION</span></span>
<span data-ttu-id="683e2-109">Questo comando ottiene lo stato della sottoscrizione per il trigger dell'evento per gli eventi del servizio esterno specificati.</span><span class="sxs-lookup"><span data-stu-id="683e2-109">This command gets the status of the subscription for the event trigger to the specified external service events.</span></span> <span data-ttu-id="683e2-110">Il trigger non può essere avviato finché lo stato restituito non è "Enabled".</span><span class="sxs-lookup"><span data-stu-id="683e2-110">The trigger can't be started until the returned status is "Enabled".</span></span>

## <span data-ttu-id="683e2-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="683e2-111">EXAMPLES</span></span>

### <span data-ttu-id="683e2-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="683e2-112">Example 1</span></span>
```
PS C:\> Get-AzDataFactoryV2TriggerSubscriptionStatus -ResourceGroupName ADF -DataFactoryName WikiADF -Name Trigger1

TriggerName Status
----------- ------
Trigger1    Enabled
```

<span data-ttu-id="683e2-113">Questo comando otterrà lo stato del trigger abbonamento for BlobEnetTrigger1 per gli eventi del servizio esterno.</span><span class="sxs-lookup"><span data-stu-id="683e2-113">This command will get the status of the subscribtion for BlobEnetTrigger1 trigger to the external service events.</span></span>

## <span data-ttu-id="683e2-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="683e2-114">PARAMETERS</span></span>

### <span data-ttu-id="683e2-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="683e2-115">-DataFactoryName</span></span>
<span data-ttu-id="683e2-116">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="683e2-116">The data factory name.</span></span>

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

### <span data-ttu-id="683e2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="683e2-117">-DefaultProfile</span></span>
<span data-ttu-id="683e2-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="683e2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="683e2-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="683e2-119">-InputObject</span></span>
<span data-ttu-id="683e2-120">Oggetto trigger.</span><span class="sxs-lookup"><span data-stu-id="683e2-120">The trigger object.</span></span>

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

### <span data-ttu-id="683e2-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="683e2-121">-Name</span></span>
<span data-ttu-id="683e2-122">Nome del trigger.</span><span class="sxs-lookup"><span data-stu-id="683e2-122">The trigger name.</span></span>

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

### <span data-ttu-id="683e2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="683e2-123">-ResourceGroupName</span></span>
<span data-ttu-id="683e2-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="683e2-124">The resource group name.</span></span>

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

### <span data-ttu-id="683e2-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="683e2-125">-ResourceId</span></span>
<span data-ttu-id="683e2-126">ID risorsa di Azure.</span><span class="sxs-lookup"><span data-stu-id="683e2-126">The Azure resource ID.</span></span>

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

### <span data-ttu-id="683e2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="683e2-127">CommonParameters</span></span>
<span data-ttu-id="683e2-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="683e2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="683e2-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="683e2-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="683e2-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="683e2-130">INPUTS</span></span>

### <span data-ttu-id="683e2-131">System. String</span><span class="sxs-lookup"><span data-stu-id="683e2-131">System.String</span></span>
<span data-ttu-id="683e2-132">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="683e2-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="683e2-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="683e2-133">OUTPUTS</span></span>

### <span data-ttu-id="683e2-134">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="683e2-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="683e2-135">Note</span><span class="sxs-lookup"><span data-stu-id="683e2-135">NOTES</span></span>

## <span data-ttu-id="683e2-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="683e2-136">RELATED LINKS</span></span>

