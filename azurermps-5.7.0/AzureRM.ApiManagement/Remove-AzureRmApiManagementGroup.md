---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: B88EC6DB-84AC-4F1D-AD79-0D243E0DC88A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementGroup.md
ms.openlocfilehash: a5919959f038b94a27f373124377466926494337
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520727"
---
# <span data-ttu-id="35380-101">Remove-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="35380-101">Remove-AzureRmApiManagementGroup</span></span>

## <span data-ttu-id="35380-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="35380-102">SYNOPSIS</span></span>
<span data-ttu-id="35380-103">Rimuove un gruppo di gestione API esistente.</span><span class="sxs-lookup"><span data-stu-id="35380-103">Removes an existing API management group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="35380-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="35380-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementGroup -Context <PsApiManagementContext> -GroupId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35380-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="35380-105">DESCRIPTION</span></span>
<span data-ttu-id="35380-106">Il cmdlet **Remove-AzureRmApiManagementGroup** rimuove un gruppo di gestione API esistente.</span><span class="sxs-lookup"><span data-stu-id="35380-106">The **Remove-AzureRmApiManagementGroup** cmdlet removes an existing API management group.</span></span>

## <span data-ttu-id="35380-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="35380-107">EXAMPLES</span></span>

### <span data-ttu-id="35380-108">Esempio 1: rimuovere un gruppo di gestione esistente</span><span class="sxs-lookup"><span data-stu-id="35380-108">Example 1: Remove an existing management group</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementGroup -Context $apimContext -GroupId "Group0001" -Force
```

<span data-ttu-id="35380-109">Questo comando rimuove un gruppo di gestione esistente denominato Group0001 e non chiede conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="35380-109">This command removes an existing management group named Group0001 and does not prompt the user for confirmation.</span></span>

## <span data-ttu-id="35380-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="35380-110">PARAMETERS</span></span>

### <span data-ttu-id="35380-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="35380-111">-Context</span></span>
<span data-ttu-id="35380-112">Specifica l'istanza di un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="35380-112">Specifies the instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="35380-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35380-113">-DefaultProfile</span></span>
<span data-ttu-id="35380-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="35380-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="35380-115">-GroupId</span><span class="sxs-lookup"><span data-stu-id="35380-115">-GroupId</span></span>
<span data-ttu-id="35380-116">Specifica l'identificatore di un gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="35380-116">Specifies the identifier of a management group.</span></span>

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

### <span data-ttu-id="35380-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="35380-117">-PassThru</span></span>
<span data-ttu-id="35380-118">Indica che questo cmdlet restituisce un valore di $True se ha esito positivo oppure un valore di $False, in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="35380-118">Indicates that this cmdlet returns a value of $True if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="35380-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="35380-119">-Confirm</span></span>
<span data-ttu-id="35380-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35380-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35380-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35380-121">-WhatIf</span></span>
<span data-ttu-id="35380-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="35380-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35380-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="35380-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35380-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35380-124">CommonParameters</span></span>
<span data-ttu-id="35380-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35380-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35380-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35380-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35380-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="35380-127">INPUTS</span></span>

### <span data-ttu-id="35380-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="35380-128">None</span></span>
<span data-ttu-id="35380-129">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="35380-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="35380-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="35380-130">OUTPUTS</span></span>

### <span data-ttu-id="35380-131">Boolean</span><span class="sxs-lookup"><span data-stu-id="35380-131">Boolean</span></span>

## <span data-ttu-id="35380-132">Note</span><span class="sxs-lookup"><span data-stu-id="35380-132">NOTES</span></span>

## <span data-ttu-id="35380-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="35380-133">RELATED LINKS</span></span>

[<span data-ttu-id="35380-134">Get-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="35380-134">Get-AzureRmApiManagementGroup</span></span>](./Get-AzureRmApiManagementGroup.md)

[<span data-ttu-id="35380-135">New-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="35380-135">New-AzureRmApiManagementGroup</span></span>](./New-AzureRmApiManagementGroup.md)

[<span data-ttu-id="35380-136">Set-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="35380-136">Set-AzureRmApiManagementGroup</span></span>](./Set-AzureRmApiManagementGroup.md)


