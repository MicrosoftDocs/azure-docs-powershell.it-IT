---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: D3C60123-CE1F-45F1-8C8F-25CDC302490C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProperty.md
ms.openlocfilehash: 333ed1cb778a5a366a7ad26d426559399658db1e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508808"
---
# <span data-ttu-id="0cb31-101">Remove-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="0cb31-101">Remove-AzureRmApiManagementProperty</span></span>

## <span data-ttu-id="0cb31-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0cb31-102">SYNOPSIS</span></span>
<span data-ttu-id="0cb31-103">Rimuove una proprietà di gestione API.</span><span class="sxs-lookup"><span data-stu-id="0cb31-103">Removes an API Management Property.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0cb31-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0cb31-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementProperty -Context <PsApiManagementContext> -PropertyId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0cb31-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0cb31-105">DESCRIPTION</span></span>
<span data-ttu-id="0cb31-106">Il cmdlet **Remove-AzureRmApiManagementProperty** rimuove una **Proprietà** di gestione delle API di Azure.</span><span class="sxs-lookup"><span data-stu-id="0cb31-106">The **Remove-AzureRmApiManagementProperty** cmdlet removes an Azure API Management **Property**.</span></span>

## <span data-ttu-id="0cb31-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0cb31-107">EXAMPLES</span></span>

### <span data-ttu-id="0cb31-108">Esempio 1: rimuovere una proprietà</span><span class="sxs-lookup"><span data-stu-id="0cb31-108">Example 1: Remove a property</span></span>
```
PS C:\>Remove-AzureRmApiManagementProperty -Context $ApimContext -PropertyId "Property11" -PassThru
```

<span data-ttu-id="0cb31-109">Questo comando rimuove la proprietà con ID Property11.</span><span class="sxs-lookup"><span data-stu-id="0cb31-109">This command removes the property that has the ID Property11.</span></span>

## <span data-ttu-id="0cb31-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0cb31-110">PARAMETERS</span></span>

### <span data-ttu-id="0cb31-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="0cb31-111">-Context</span></span>
<span data-ttu-id="0cb31-112">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="0cb31-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="0cb31-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0cb31-113">-PassThru</span></span>
<span data-ttu-id="0cb31-114">Indica che questo cmdlet restituisce un valore di $True se l'operazione viene eseguita correttamente o $False in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="0cb31-114">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="0cb31-115">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="0cb31-115">-PropertyId</span></span>
<span data-ttu-id="0cb31-116">Specifica un ID della proprietà rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0cb31-116">Specifies an ID of the property that this cmdlet removes.</span></span>

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

### <span data-ttu-id="0cb31-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0cb31-117">-Confirm</span></span>
<span data-ttu-id="0cb31-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0cb31-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0cb31-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0cb31-119">-WhatIf</span></span>
<span data-ttu-id="0cb31-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0cb31-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0cb31-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0cb31-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0cb31-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cb31-122">-DefaultProfile</span></span>
<span data-ttu-id="0cb31-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0cb31-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0cb31-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cb31-124">CommonParameters</span></span>
<span data-ttu-id="0cb31-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0cb31-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cb31-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0cb31-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cb31-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0cb31-127">INPUTS</span></span>

## <span data-ttu-id="0cb31-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0cb31-128">OUTPUTS</span></span>

### <span data-ttu-id="0cb31-129">bool</span><span class="sxs-lookup"><span data-stu-id="0cb31-129">bool</span></span>

## <span data-ttu-id="0cb31-130">Note</span><span class="sxs-lookup"><span data-stu-id="0cb31-130">NOTES</span></span>

## <span data-ttu-id="0cb31-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0cb31-131">RELATED LINKS</span></span>

[<span data-ttu-id="0cb31-132">New-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="0cb31-132">New-AzureRmApiManagementProperty</span></span>](./New-AzureRmApiManagementProperty.md)

[<span data-ttu-id="0cb31-133">Set-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="0cb31-133">Set-AzureRmApiManagementProperty</span></span>](./Set-AzureRmApiManagementProperty.md)


