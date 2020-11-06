---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 66D543C0-34F0-47B1-943A-415DECF2155C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementGroup.md
ms.openlocfilehash: 20f2f79c154cd16dcf09501bdbefb488fdeb61eb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515836"
---
# <span data-ttu-id="e177c-101">Set-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="e177c-101">Set-AzureRmApiManagementGroup</span></span>

## <span data-ttu-id="e177c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e177c-102">SYNOPSIS</span></span>
<span data-ttu-id="e177c-103">Configura un gruppo di gestione API.</span><span class="sxs-lookup"><span data-stu-id="e177c-103">Configures an API management group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e177c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e177c-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementGroup -Context <PsApiManagementContext> -GroupId <String> [-Name <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e177c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e177c-105">DESCRIPTION</span></span>
<span data-ttu-id="e177c-106">Il cmdlet **set-AzureRmApiManagementGroup** configura un gruppo di gestione API.</span><span class="sxs-lookup"><span data-stu-id="e177c-106">The **Set-AzureRmApiManagementGroup** cmdlet configures an API management group.</span></span>

## <span data-ttu-id="e177c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e177c-107">EXAMPLES</span></span>

### <span data-ttu-id="e177c-108">Esempio 1: configurare un gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="e177c-108">Example 1: Configure a management group</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementGroup -Context $apimContext -Description "Updated Management Group" -Name "Group0001"
```

<span data-ttu-id="e177c-109">Questo comando configura un gruppo di gestione denominato Group0001.</span><span class="sxs-lookup"><span data-stu-id="e177c-109">This command configures a management group named Group0001.</span></span>

## <span data-ttu-id="e177c-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e177c-110">PARAMETERS</span></span>

### <span data-ttu-id="e177c-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="e177c-111">-Context</span></span>
<span data-ttu-id="e177c-112">Specifica un'istanza di un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="e177c-112">Specifies an instance of a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e177c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e177c-113">-DefaultProfile</span></span>
<span data-ttu-id="e177c-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e177c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="e177c-115">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="e177c-115">-Description</span></span>
<span data-ttu-id="e177c-116">Specifica la descrizione del gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="e177c-116">Specifies the description of the management group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e177c-117">-GroupId</span><span class="sxs-lookup"><span data-stu-id="e177c-117">-GroupId</span></span>
<span data-ttu-id="e177c-118">Specifica l'identificatore del gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="e177c-118">Specifies the identifier of the management group.</span></span>

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

### <span data-ttu-id="e177c-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="e177c-119">-Name</span></span>
<span data-ttu-id="e177c-120">Specifica il nome del gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="e177c-120">Specifies the name of the management group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e177c-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e177c-121">-PassThru</span></span>
<span data-ttu-id="e177c-122">PassThru</span><span class="sxs-lookup"><span data-stu-id="e177c-122">passthru</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e177c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e177c-123">CommonParameters</span></span>
<span data-ttu-id="e177c-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e177c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e177c-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e177c-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e177c-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e177c-126">INPUTS</span></span>

### <span data-ttu-id="e177c-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e177c-127">None</span></span>
<span data-ttu-id="e177c-128">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="e177c-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e177c-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e177c-129">OUTPUTS</span></span>

### <span data-ttu-id="e177c-130">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="e177c-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="e177c-131">Note</span><span class="sxs-lookup"><span data-stu-id="e177c-131">NOTES</span></span>

## <span data-ttu-id="e177c-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e177c-132">RELATED LINKS</span></span>

[<span data-ttu-id="e177c-133">Get-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="e177c-133">Get-AzureRmApiManagementGroup</span></span>](./Get-AzureRmApiManagementGroup.md)

[<span data-ttu-id="e177c-134">New-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="e177c-134">New-AzureRmApiManagementGroup</span></span>](./New-AzureRmApiManagementGroup.md)

[<span data-ttu-id="e177c-135">Remove-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="e177c-135">Remove-AzureRmApiManagementGroup</span></span>](./Remove-AzureRmApiManagementGroup.md)


