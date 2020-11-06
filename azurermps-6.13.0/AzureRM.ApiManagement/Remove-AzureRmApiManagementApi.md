---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: F23D9274-63B9-4654-897B-6E84757774D2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApi.md
ms.openlocfilehash: cf27d54e50d320d0ad20a3e847cf2b9dda8ac3c3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519312"
---
# <span data-ttu-id="0ac94-101">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="0ac94-101">Remove-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="0ac94-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0ac94-102">SYNOPSIS</span></span>
<span data-ttu-id="0ac94-103">Rimuove un'API.</span><span class="sxs-lookup"><span data-stu-id="0ac94-103">Removes an API.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0ac94-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0ac94-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ac94-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0ac94-105">DESCRIPTION</span></span>
<span data-ttu-id="0ac94-106">Il cmdlet **Remove-AzureRmApiManagementApi** rimuove un'API esistente.</span><span class="sxs-lookup"><span data-stu-id="0ac94-106">The **Remove-AzureRmApiManagementApi** cmdlet removes an existing API.</span></span>

## <span data-ttu-id="0ac94-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0ac94-107">EXAMPLES</span></span>

### <span data-ttu-id="0ac94-108">Esempio 1: rimuovere un'API</span><span class="sxs-lookup"><span data-stu-id="0ac94-108">Example 1: Remove an API</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementApi -Context $apimContext -ApiId "0123456789"
```

<span data-ttu-id="0ac94-109">Questo comando rimuove l'API con l'ID specificato.</span><span class="sxs-lookup"><span data-stu-id="0ac94-109">This command removes the API with the specified ID.</span></span>

## <span data-ttu-id="0ac94-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0ac94-110">PARAMETERS</span></span>

### <span data-ttu-id="0ac94-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="0ac94-111">-ApiId</span></span>
<span data-ttu-id="0ac94-112">Specifica l'ID dell'API Remove.</span><span class="sxs-lookup"><span data-stu-id="0ac94-112">Specifies the ID of the API remove.</span></span>

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

### <span data-ttu-id="0ac94-113">-Contesto</span><span class="sxs-lookup"><span data-stu-id="0ac94-113">-Context</span></span>
<span data-ttu-id="0ac94-114">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="0ac94-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="0ac94-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ac94-115">-DefaultProfile</span></span>
<span data-ttu-id="0ac94-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0ac94-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ac94-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0ac94-117">-PassThru</span></span>
<span data-ttu-id="0ac94-118">PassThru</span><span class="sxs-lookup"><span data-stu-id="0ac94-118">passthru</span></span>

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

### <span data-ttu-id="0ac94-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0ac94-119">-Confirm</span></span>
<span data-ttu-id="0ac94-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0ac94-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ac94-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ac94-121">-WhatIf</span></span>
<span data-ttu-id="0ac94-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0ac94-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ac94-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0ac94-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ac94-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ac94-124">CommonParameters</span></span>
<span data-ttu-id="0ac94-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ac94-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ac94-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ac94-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ac94-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0ac94-127">INPUTS</span></span>

### <span data-ttu-id="0ac94-128">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="0ac94-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="0ac94-129">System. String</span><span class="sxs-lookup"><span data-stu-id="0ac94-129">System.String</span></span>

### <span data-ttu-id="0ac94-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0ac94-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0ac94-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0ac94-131">OUTPUTS</span></span>

### <span data-ttu-id="0ac94-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0ac94-132">System.Boolean</span></span>

## <span data-ttu-id="0ac94-133">Note</span><span class="sxs-lookup"><span data-stu-id="0ac94-133">NOTES</span></span>

## <span data-ttu-id="0ac94-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0ac94-134">RELATED LINKS</span></span>

[<span data-ttu-id="0ac94-135">Export-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="0ac94-135">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="0ac94-136">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="0ac94-136">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="0ac94-137">Import-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="0ac94-137">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="0ac94-138">New-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="0ac94-138">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="0ac94-139">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="0ac94-139">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


