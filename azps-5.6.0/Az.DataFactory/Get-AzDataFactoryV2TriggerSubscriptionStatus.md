---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactoryv2triggersubscriptionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2TriggerSubscriptionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2TriggerSubscriptionStatus.md
ms.openlocfilehash: a83028b47d487f4bbb2732497d7e9eefd01882ce
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975117"
---
# <span data-ttu-id="25174-101">Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="25174-101">Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>

## <span data-ttu-id="25174-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25174-102">SYNOPSIS</span></span>
<span data-ttu-id="25174-103">Ottenere lo stato della sottoscrizione per il trigger di evento per gli eventi del servizio esterno specificati.</span><span class="sxs-lookup"><span data-stu-id="25174-103">Get the status of the subscription for the event trigger to the specified external service events.</span></span>

## <span data-ttu-id="25174-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="25174-104">SYNTAX</span></span>

### <span data-ttu-id="25174-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="25174-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2TriggerSubscriptionStatus [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25174-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="25174-106">ByInputObject</span></span>
```
Get-AzDataFactoryV2TriggerSubscriptionStatus [-InputObject] <PSTrigger>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25174-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="25174-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2TriggerSubscriptionStatus [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="25174-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="25174-108">DESCRIPTION</span></span>
<span data-ttu-id="25174-109">Questo comando recupera lo stato della sottoscrizione per il trigger di evento per gli eventi del servizio esterno specificati.</span><span class="sxs-lookup"><span data-stu-id="25174-109">This command gets the status of the subscription for the event trigger to the specified external service events.</span></span> <span data-ttu-id="25174-110">Il trigger non può essere avviato finché lo stato restituito non è "Abilitato".</span><span class="sxs-lookup"><span data-stu-id="25174-110">The trigger can't be started until the returned status is "Enabled".</span></span>

## <span data-ttu-id="25174-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="25174-111">EXAMPLES</span></span>

### <span data-ttu-id="25174-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="25174-112">Example 1</span></span>
```
PS C:\> Get-AzDataFactoryV2TriggerSubscriptionStatus -ResourceGroupName ADF -DataFactoryName WikiADF -Name Trigger1

TriggerName Status
----------- ------
Trigger1    Enabled
```

<span data-ttu-id="25174-113">Questo comando ottiene lo stato del trigger BlobEnetTrigger1 per la sottoscrizione per gli eventi del servizio esterno.</span><span class="sxs-lookup"><span data-stu-id="25174-113">This command will get the status of the subscribtion for BlobEnetTrigger1 trigger to the external service events.</span></span>

## <span data-ttu-id="25174-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="25174-114">PARAMETERS</span></span>

### <span data-ttu-id="25174-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="25174-115">-DataFactoryName</span></span>
<span data-ttu-id="25174-116">Nome del data factory.</span><span class="sxs-lookup"><span data-stu-id="25174-116">The data factory name.</span></span>

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

### <span data-ttu-id="25174-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25174-117">-DefaultProfile</span></span>
<span data-ttu-id="25174-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="25174-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25174-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="25174-119">-InputObject</span></span>
<span data-ttu-id="25174-120">Oggetto trigger.</span><span class="sxs-lookup"><span data-stu-id="25174-120">The trigger object.</span></span>

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

### <span data-ttu-id="25174-121">-Name</span><span class="sxs-lookup"><span data-stu-id="25174-121">-Name</span></span>
<span data-ttu-id="25174-122">Nome del trigger.</span><span class="sxs-lookup"><span data-stu-id="25174-122">The trigger name.</span></span>

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

### <span data-ttu-id="25174-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25174-123">-ResourceGroupName</span></span>
<span data-ttu-id="25174-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="25174-124">The resource group name.</span></span>

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

### <span data-ttu-id="25174-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="25174-125">-ResourceId</span></span>
<span data-ttu-id="25174-126">ID della risorsa Azure.</span><span class="sxs-lookup"><span data-stu-id="25174-126">The Azure resource ID.</span></span>

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

### <span data-ttu-id="25174-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25174-127">CommonParameters</span></span>
<span data-ttu-id="25174-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25174-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25174-129">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25174-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25174-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="25174-130">INPUTS</span></span>

### <span data-ttu-id="25174-131">System.String</span><span class="sxs-lookup"><span data-stu-id="25174-131">System.String</span></span>
<span data-ttu-id="25174-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span><span class="sxs-lookup"><span data-stu-id="25174-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="25174-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="25174-133">OUTPUTS</span></span>

### <span data-ttu-id="25174-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="25174-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="25174-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="25174-135">NOTES</span></span>

## <span data-ttu-id="25174-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="25174-136">RELATED LINKS</span></span>

