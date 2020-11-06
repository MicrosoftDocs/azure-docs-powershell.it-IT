---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 98AD1C84-B147-48EB-94B5-8D77B531F6F8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementLogger.md
ms.openlocfilehash: 3c36d0b21b1fdda1282a1184f90728e827515195
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511383"
---
# <span data-ttu-id="7dd3d-101">Remove-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="7dd3d-101">Remove-AzureRmApiManagementLogger</span></span>

## <span data-ttu-id="7dd3d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7dd3d-102">SYNOPSIS</span></span>
<span data-ttu-id="7dd3d-103">Rimuove un logger di gestione API.</span><span class="sxs-lookup"><span data-stu-id="7dd3d-103">Removes an API Management Logger.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7dd3d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7dd3d-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7dd3d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7dd3d-105">DESCRIPTION</span></span>
<span data-ttu-id="7dd3d-106">Il cmdlet **Remove-AzureRmApiManagementLogger** rimuove un **logger** di gestione delle API di Azure.</span><span class="sxs-lookup"><span data-stu-id="7dd3d-106">The **Remove-AzureRmApiManagementLogger** cmdlet removes an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="7dd3d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7dd3d-107">EXAMPLES</span></span>

### <span data-ttu-id="7dd3d-108">Esempio 1: rimuovere un logger</span><span class="sxs-lookup"><span data-stu-id="7dd3d-108">Example 1: Remove a logger</span></span>
```
PS C:\>Remove-AzureRmApiManagementLogger -Context $ApimContext -LoggerId "Logger123" -Force
```

<span data-ttu-id="7dd3d-109">Questo comando rimuove un logger con ID Logger123.</span><span class="sxs-lookup"><span data-stu-id="7dd3d-109">This command removes a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="7dd3d-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7dd3d-110">PARAMETERS</span></span>

### <span data-ttu-id="7dd3d-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="7dd3d-111">-Context</span></span>
<span data-ttu-id="7dd3d-112">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="7dd3d-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="7dd3d-113">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="7dd3d-113">-LoggerId</span></span>
<span data-ttu-id="7dd3d-114">Specifica l'ID del logger da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="7dd3d-114">Specifies the ID of the logger to remove.</span></span>

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

### <span data-ttu-id="7dd3d-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7dd3d-115">-PassThru</span></span>
<span data-ttu-id="7dd3d-116">Indica che questo cmdlet restituisce un valore di $True se l'operazione viene eseguita correttamente o $False in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="7dd3d-116">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="7dd3d-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7dd3d-117">-Confirm</span></span>
<span data-ttu-id="7dd3d-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7dd3d-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7dd3d-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7dd3d-119">-WhatIf</span></span>
<span data-ttu-id="7dd3d-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7dd3d-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7dd3d-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7dd3d-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7dd3d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7dd3d-122">-DefaultProfile</span></span>
<span data-ttu-id="7dd3d-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7dd3d-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7dd3d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7dd3d-124">CommonParameters</span></span>
<span data-ttu-id="7dd3d-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7dd3d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7dd3d-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7dd3d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7dd3d-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7dd3d-127">INPUTS</span></span>

## <span data-ttu-id="7dd3d-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7dd3d-128">OUTPUTS</span></span>

### <span data-ttu-id="7dd3d-129">Boolean</span><span class="sxs-lookup"><span data-stu-id="7dd3d-129">Boolean</span></span>

## <span data-ttu-id="7dd3d-130">Note</span><span class="sxs-lookup"><span data-stu-id="7dd3d-130">NOTES</span></span>

## <span data-ttu-id="7dd3d-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7dd3d-131">RELATED LINKS</span></span>

[<span data-ttu-id="7dd3d-132">Get-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="7dd3d-132">Get-AzureRmApiManagementLogger</span></span>](./Get-AzureRmApiManagementLogger.md)

[<span data-ttu-id="7dd3d-133">New-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="7dd3d-133">New-AzureRmApiManagementLogger</span></span>](./New-AzureRmApiManagementLogger.md)

[<span data-ttu-id="7dd3d-134">Set-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="7dd3d-134">Set-AzureRmApiManagementLogger</span></span>](./Set-AzureRmApiManagementLogger.md)


