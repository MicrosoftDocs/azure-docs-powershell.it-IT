---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: A4A8D996-72A2-4154-98DA-5F84CAA010B9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementOperation.md
ms.openlocfilehash: ef3db99522c07b593493e30bd3778f1774af1a5f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520728"
---
# <span data-ttu-id="79137-101">Remove-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="79137-101">Remove-AzureRmApiManagementOperation</span></span>

## <span data-ttu-id="79137-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="79137-102">SYNOPSIS</span></span>
<span data-ttu-id="79137-103">Rimuove un'operazione esistente.</span><span class="sxs-lookup"><span data-stu-id="79137-103">Removes an existing operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="79137-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="79137-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> -OperationId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79137-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="79137-105">DESCRIPTION</span></span>
<span data-ttu-id="79137-106">Il cmdlet **Remove-AzureRmApiManagementOperation** rimuove un'operazione esistente.</span><span class="sxs-lookup"><span data-stu-id="79137-106">The **Remove-AzureRmApiManagementOperation** cmdlet removes an existing operation.</span></span>

## <span data-ttu-id="79137-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="79137-107">EXAMPLES</span></span>

### <span data-ttu-id="79137-108">Esempio 1: rimuovere un'operazione API esistente</span><span class="sxs-lookup"><span data-stu-id="79137-108">Example 1: Remove an existing API Operation</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementOperation -Context $apimContext -ApiId "0123456789" -OperationId "9876543210" -Force
```

<span data-ttu-id="79137-109">Questo comando rimuove un'operazione API esistente.</span><span class="sxs-lookup"><span data-stu-id="79137-109">This command removes an existing API Operation.</span></span>

## <span data-ttu-id="79137-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="79137-110">PARAMETERS</span></span>

### <span data-ttu-id="79137-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="79137-111">-ApiId</span></span>
<span data-ttu-id="79137-112">Specifica l'identificatore dell'API.</span><span class="sxs-lookup"><span data-stu-id="79137-112">Specifies the identifier of the API.</span></span>

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

### <span data-ttu-id="79137-113">-Contesto</span><span class="sxs-lookup"><span data-stu-id="79137-113">-Context</span></span>
<span data-ttu-id="79137-114">Specifica un'istanza di **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="79137-114">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="79137-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79137-115">-DefaultProfile</span></span>
<span data-ttu-id="79137-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="79137-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="79137-117">-OperationId</span><span class="sxs-lookup"><span data-stu-id="79137-117">-OperationId</span></span>
<span data-ttu-id="79137-118">Specifica l'identificatore dell'operazione API.</span><span class="sxs-lookup"><span data-stu-id="79137-118">Specifies the identifier of the API operation.</span></span>

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

### <span data-ttu-id="79137-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="79137-119">-PassThru</span></span>
<span data-ttu-id="79137-120">Indica che questo cmdlet restituisce un valore di $True se ha esito positivo oppure un valore di $False, in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="79137-120">Indicates that this cmdlet returns a value of $True if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="79137-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="79137-121">-Confirm</span></span>
<span data-ttu-id="79137-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79137-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79137-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79137-123">-WhatIf</span></span>
<span data-ttu-id="79137-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="79137-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79137-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="79137-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79137-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79137-126">CommonParameters</span></span>
<span data-ttu-id="79137-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79137-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79137-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79137-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79137-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="79137-129">INPUTS</span></span>

### <span data-ttu-id="79137-130">Nessuno</span><span class="sxs-lookup"><span data-stu-id="79137-130">None</span></span>
<span data-ttu-id="79137-131">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="79137-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="79137-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="79137-132">OUTPUTS</span></span>

### <span data-ttu-id="79137-133">bool</span><span class="sxs-lookup"><span data-stu-id="79137-133">bool</span></span>

## <span data-ttu-id="79137-134">Note</span><span class="sxs-lookup"><span data-stu-id="79137-134">NOTES</span></span>

## <span data-ttu-id="79137-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="79137-135">RELATED LINKS</span></span>

[<span data-ttu-id="79137-136">Get-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="79137-136">Get-AzureRmApiManagementOperation</span></span>](./Get-AzureRmApiManagementOperation.md)

[<span data-ttu-id="79137-137">New-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="79137-137">New-AzureRmApiManagementOperation</span></span>](./New-AzureRmApiManagementOperation.md)

[<span data-ttu-id="79137-138">Set-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="79137-138">Set-AzureRmApiManagementOperation</span></span>](./Set-AzureRmApiManagementOperation.md)


