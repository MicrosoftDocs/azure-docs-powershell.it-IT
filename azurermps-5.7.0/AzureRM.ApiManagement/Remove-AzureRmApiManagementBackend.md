---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementBackend.md
ms.openlocfilehash: 347a05c5e197a93458a64c4079ce1fd430e631f4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515843"
---
# <span data-ttu-id="01714-101">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="01714-101">Remove-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="01714-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="01714-102">SYNOPSIS</span></span>
<span data-ttu-id="01714-103">Rimuove un backend.</span><span class="sxs-lookup"><span data-stu-id="01714-103">Removes a Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="01714-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="01714-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01714-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="01714-105">DESCRIPTION</span></span>
<span data-ttu-id="01714-106">Rimuove un backend specificato dall'identificatore dalla gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="01714-106">Removes a backend specified by the Identifier from the Api Management.</span></span>

## <span data-ttu-id="01714-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="01714-107">EXAMPLES</span></span>

### <span data-ttu-id="01714-108">Esempio 1: rimuovere il backend 123</span><span class="sxs-lookup"><span data-stu-id="01714-108">Example 1: Remove the Backend 123</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementBackend -Context $apimContext -BackendId 123 -PassThru
```

## <span data-ttu-id="01714-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="01714-109">PARAMETERS</span></span>

### <span data-ttu-id="01714-110">-BackendId</span><span class="sxs-lookup"><span data-stu-id="01714-110">-BackendId</span></span>
<span data-ttu-id="01714-111">Identificatore del backend esistente.</span><span class="sxs-lookup"><span data-stu-id="01714-111">Identifier of existing backend.</span></span>
<span data-ttu-id="01714-112">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="01714-112">This parameter is required.</span></span>

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

### <span data-ttu-id="01714-113">-Contesto</span><span class="sxs-lookup"><span data-stu-id="01714-113">-Context</span></span>
<span data-ttu-id="01714-114">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="01714-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="01714-115">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="01714-115">This parameter is required.</span></span>

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

### <span data-ttu-id="01714-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01714-116">-DefaultProfile</span></span>
<span data-ttu-id="01714-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="01714-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="01714-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="01714-118">-PassThru</span></span>
<span data-ttu-id="01714-119">Se specificato scriverà true nel caso in cui l'operazione venga eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="01714-119">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="01714-120">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="01714-120">This parameter is optional.</span></span>
<span data-ttu-id="01714-121">Il valore predefinito è false.</span><span class="sxs-lookup"><span data-stu-id="01714-121">Default value is false.</span></span>

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

### <span data-ttu-id="01714-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="01714-122">-Confirm</span></span>
<span data-ttu-id="01714-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="01714-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01714-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01714-124">-WhatIf</span></span>
<span data-ttu-id="01714-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="01714-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="01714-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="01714-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01714-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01714-127">CommonParameters</span></span>
<span data-ttu-id="01714-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01714-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01714-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01714-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01714-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="01714-130">INPUTS</span></span>

### <span data-ttu-id="01714-131">Nessuno</span><span class="sxs-lookup"><span data-stu-id="01714-131">None</span></span>
<span data-ttu-id="01714-132">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="01714-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="01714-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="01714-133">OUTPUTS</span></span>

### <span data-ttu-id="01714-134">bool</span><span class="sxs-lookup"><span data-stu-id="01714-134">bool</span></span>

## <span data-ttu-id="01714-135">Note</span><span class="sxs-lookup"><span data-stu-id="01714-135">NOTES</span></span>

## <span data-ttu-id="01714-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="01714-136">RELATED LINKS</span></span>

[<span data-ttu-id="01714-137">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="01714-137">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="01714-138">New-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="01714-138">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="01714-139">New-AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="01714-139">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="01714-140">New-AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="01714-140">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="01714-141">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="01714-141">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)
