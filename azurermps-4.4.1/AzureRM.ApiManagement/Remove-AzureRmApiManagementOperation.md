---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: A4A8D996-72A2-4154-98DA-5F84CAA010B9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementOperation.md
ms.openlocfilehash: 685da9955f272066ec39890ea0f3a063d3b2f9b8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510784"
---
# <span data-ttu-id="e0078-101">Remove-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="e0078-101">Remove-AzureRmApiManagementOperation</span></span>

## <span data-ttu-id="e0078-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e0078-102">SYNOPSIS</span></span>
<span data-ttu-id="e0078-103">Rimuove un'operazione esistente.</span><span class="sxs-lookup"><span data-stu-id="e0078-103">Removes an existing operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e0078-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e0078-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> -OperationId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0078-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e0078-105">DESCRIPTION</span></span>
<span data-ttu-id="e0078-106">Il cmdlet **Remove-AzureRmApiManagementOperation** rimuove un'operazione esistente.</span><span class="sxs-lookup"><span data-stu-id="e0078-106">The **Remove-AzureRmApiManagementOperation** cmdlet removes an existing operation.</span></span>

## <span data-ttu-id="e0078-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e0078-107">EXAMPLES</span></span>

### <span data-ttu-id="e0078-108">Esempio 1: rimuovere un'operazione API esistente</span><span class="sxs-lookup"><span data-stu-id="e0078-108">Example 1: Remove an existing API Operation</span></span>
```
PS C:\>Remove-AzureRmApiManagementOperation -Context $APImContext -ApiId "0123456789" -OperationId "9876543210" -Force
```

<span data-ttu-id="e0078-109">Questo comando rimuove un'operazione API esistente.</span><span class="sxs-lookup"><span data-stu-id="e0078-109">This command removes an existing API Operation.</span></span>

## <span data-ttu-id="e0078-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e0078-110">PARAMETERS</span></span>

### <span data-ttu-id="e0078-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="e0078-111">-ApiId</span></span>
<span data-ttu-id="e0078-112">Specifica l'identificatore dell'API.</span><span class="sxs-lookup"><span data-stu-id="e0078-112">Specifies the identifier of the API.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0078-113">-Contesto</span><span class="sxs-lookup"><span data-stu-id="e0078-113">-Context</span></span>
<span data-ttu-id="e0078-114">Specifica un'istanza di **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="e0078-114">Specifies an instance of **PsApiManagementContext**.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0078-115">-OperationId</span><span class="sxs-lookup"><span data-stu-id="e0078-115">-OperationId</span></span>
<span data-ttu-id="e0078-116">Specifica l'identificatore dell'operazione API.</span><span class="sxs-lookup"><span data-stu-id="e0078-116">Specifies the identifier of the API operation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0078-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e0078-117">-PassThru</span></span>
<span data-ttu-id="e0078-118">Indica che questo cmdlet restituisce un valore di $True se ha esito positivo oppure un valore di $False, in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="e0078-118">Indicates that this cmdlet returns a value of $True if it succeeds, or a value of $False, otherwise.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0078-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e0078-119">-Confirm</span></span>
<span data-ttu-id="e0078-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0078-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0078-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0078-121">-WhatIf</span></span>
<span data-ttu-id="e0078-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e0078-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0078-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e0078-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0078-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0078-124">-DefaultProfile</span></span>
<span data-ttu-id="e0078-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e0078-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0078-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0078-126">CommonParameters</span></span>
<span data-ttu-id="e0078-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0078-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0078-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0078-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0078-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e0078-129">INPUTS</span></span>

## <span data-ttu-id="e0078-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e0078-130">OUTPUTS</span></span>

### <span data-ttu-id="e0078-131">bool</span><span class="sxs-lookup"><span data-stu-id="e0078-131">bool</span></span>

## <span data-ttu-id="e0078-132">Note</span><span class="sxs-lookup"><span data-stu-id="e0078-132">NOTES</span></span>

## <span data-ttu-id="e0078-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e0078-133">RELATED LINKS</span></span>

[<span data-ttu-id="e0078-134">Get-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="e0078-134">Get-AzureRmApiManagementOperation</span></span>](./Get-AzureRmApiManagementOperation.md)

[<span data-ttu-id="e0078-135">New-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="e0078-135">New-AzureRmApiManagementOperation</span></span>](./New-AzureRmApiManagementOperation.md)

[<span data-ttu-id="e0078-136">Set-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="e0078-136">Set-AzureRmApiManagementOperation</span></span>](./Set-AzureRmApiManagementOperation.md)


