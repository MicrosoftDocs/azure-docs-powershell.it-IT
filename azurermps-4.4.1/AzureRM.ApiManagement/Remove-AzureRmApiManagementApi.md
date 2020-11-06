---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: F23D9274-63B9-4654-897B-6E84757774D2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApi.md
ms.openlocfilehash: cadae96af05ae11f76d3a8ea0010da4d73161186
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508828"
---
# <span data-ttu-id="5110f-101">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="5110f-101">Remove-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="5110f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5110f-102">SYNOPSIS</span></span>
<span data-ttu-id="5110f-103">Rimuove un'API.</span><span class="sxs-lookup"><span data-stu-id="5110f-103">Removes an API.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5110f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5110f-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5110f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5110f-105">DESCRIPTION</span></span>
<span data-ttu-id="5110f-106">Il cmdlet **Remove-AzureRmApiManagementApi** rimuove un'API esistente.</span><span class="sxs-lookup"><span data-stu-id="5110f-106">The **Remove-AzureRmApiManagementApi** cmdlet removes an existing API.</span></span>

## <span data-ttu-id="5110f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5110f-107">EXAMPLES</span></span>

### <span data-ttu-id="5110f-108">Esempio 1: rimuovere un'API</span><span class="sxs-lookup"><span data-stu-id="5110f-108">Example 1: Remove an API</span></span>
```
PS C:\>Remove-AzureRmApiManagementApi -Context $ApiMgmtContext -ApiId "0123456789"
```

<span data-ttu-id="5110f-109">Questo comando rimuove l'API con l'ID specificato.</span><span class="sxs-lookup"><span data-stu-id="5110f-109">This command removes the API with the specified ID.</span></span>

## <span data-ttu-id="5110f-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5110f-110">PARAMETERS</span></span>

### <span data-ttu-id="5110f-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="5110f-111">-ApiId</span></span>
<span data-ttu-id="5110f-112">Specifica l'ID dell'API Remove.</span><span class="sxs-lookup"><span data-stu-id="5110f-112">Specifies the ID of the API remove.</span></span>

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

### <span data-ttu-id="5110f-113">-Contesto</span><span class="sxs-lookup"><span data-stu-id="5110f-113">-Context</span></span>
<span data-ttu-id="5110f-114">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="5110f-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="5110f-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5110f-115">-PassThru</span></span>
<span data-ttu-id="5110f-116">PassThru</span><span class="sxs-lookup"><span data-stu-id="5110f-116">passthru</span></span>

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

### <span data-ttu-id="5110f-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5110f-117">-Confirm</span></span>
<span data-ttu-id="5110f-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5110f-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5110f-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5110f-119">-WhatIf</span></span>
<span data-ttu-id="5110f-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5110f-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5110f-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5110f-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5110f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5110f-122">-DefaultProfile</span></span>
<span data-ttu-id="5110f-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5110f-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5110f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5110f-124">CommonParameters</span></span>
<span data-ttu-id="5110f-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5110f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5110f-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5110f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5110f-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5110f-127">INPUTS</span></span>

## <span data-ttu-id="5110f-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5110f-128">OUTPUTS</span></span>

### <span data-ttu-id="5110f-129">Boolean</span><span class="sxs-lookup"><span data-stu-id="5110f-129">Boolean</span></span>

## <span data-ttu-id="5110f-130">Note</span><span class="sxs-lookup"><span data-stu-id="5110f-130">NOTES</span></span>

## <span data-ttu-id="5110f-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5110f-131">RELATED LINKS</span></span>

[<span data-ttu-id="5110f-132">Export-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="5110f-132">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="5110f-133">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="5110f-133">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="5110f-134">Import-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="5110f-134">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="5110f-135">New-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="5110f-135">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="5110f-136">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="5110f-136">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


