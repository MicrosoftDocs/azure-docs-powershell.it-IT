---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A4A8D996-72A2-4154-98DA-5F84CAA010B9
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementOperation.md
ms.openlocfilehash: 153eb354ae8ba0f033a34010658b0d851572ddd6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98331660"
---
# <span data-ttu-id="4b553-101">Remove-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="4b553-101">Remove-AzApiManagementOperation</span></span>

## <span data-ttu-id="4b553-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4b553-102">SYNOPSIS</span></span>
<span data-ttu-id="4b553-103">Rimuove un'operazione esistente.</span><span class="sxs-lookup"><span data-stu-id="4b553-103">Removes an existing operation.</span></span>

## <span data-ttu-id="4b553-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4b553-104">SYNTAX</span></span>

```
Remove-AzApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -OperationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4b553-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4b553-105">DESCRIPTION</span></span>
<span data-ttu-id="4b553-106">Il cmdlet **Remove-AzApiManagementOperation** rimuove un'operazione esistente.</span><span class="sxs-lookup"><span data-stu-id="4b553-106">The **Remove-AzApiManagementOperation** cmdlet removes an existing operation.</span></span>

## <span data-ttu-id="4b553-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4b553-107">EXAMPLES</span></span>

### <span data-ttu-id="4b553-108">Esempio 1: rimuovere un'operazione API esistente</span><span class="sxs-lookup"><span data-stu-id="4b553-108">Example 1: Remove an existing API Operation</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementOperation -Context $apimContext -ApiId "0123456789" -OperationId "9876543210" -Force
```

<span data-ttu-id="4b553-109">Questo comando rimuove un'operazione API esistente.</span><span class="sxs-lookup"><span data-stu-id="4b553-109">This command removes an existing API Operation.</span></span>

## <span data-ttu-id="4b553-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4b553-110">PARAMETERS</span></span>

### <span data-ttu-id="4b553-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="4b553-111">-ApiId</span></span>
<span data-ttu-id="4b553-112">Specifica l'identificatore dell'API.</span><span class="sxs-lookup"><span data-stu-id="4b553-112">Specifies the identifier of the API.</span></span>

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

### <span data-ttu-id="4b553-113">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="4b553-113">-ApiRevision</span></span>
<span data-ttu-id="4b553-114">Identificatore della revisione API.</span><span class="sxs-lookup"><span data-stu-id="4b553-114">Identifier of API Revision.</span></span> <span data-ttu-id="4b553-115">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="4b553-115">This parameter is optional.</span></span> <span data-ttu-id="4b553-116">Se non specificato, l'operazione verrà rimossa dalla revisione API attualmente attiva.</span><span class="sxs-lookup"><span data-stu-id="4b553-116">If not specified, the operation will be removed from the currently active api revision.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b553-117">-Contesto</span><span class="sxs-lookup"><span data-stu-id="4b553-117">-Context</span></span>
<span data-ttu-id="4b553-118">Specifica un'istanza di **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="4b553-118">Specifies an instance of **PsApiManagementContext**.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4b553-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b553-119">-DefaultProfile</span></span>
<span data-ttu-id="4b553-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4b553-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b553-121">-OperationId</span><span class="sxs-lookup"><span data-stu-id="4b553-121">-OperationId</span></span>
<span data-ttu-id="4b553-122">Specifica l'identificatore dell'operazione API.</span><span class="sxs-lookup"><span data-stu-id="4b553-122">Specifies the identifier of the API operation.</span></span>

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

### <span data-ttu-id="4b553-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4b553-123">-PassThru</span></span>
<span data-ttu-id="4b553-124">Indica che questo cmdlet restituisce un valore di $True se ha esito positivo oppure un valore di $False, in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="4b553-124">Indicates that this cmdlet returns a value of $True if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="4b553-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4b553-125">-Confirm</span></span>
<span data-ttu-id="4b553-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4b553-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b553-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b553-127">-WhatIf</span></span>
<span data-ttu-id="4b553-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4b553-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b553-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4b553-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b553-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b553-130">CommonParameters</span></span>
<span data-ttu-id="4b553-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b553-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b553-132">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4b553-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b553-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4b553-133">INPUTS</span></span>

### <span data-ttu-id="4b553-134">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="4b553-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="4b553-135">System. String</span><span class="sxs-lookup"><span data-stu-id="4b553-135">System.String</span></span>

### <span data-ttu-id="4b553-136">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4b553-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4b553-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4b553-137">OUTPUTS</span></span>

### <span data-ttu-id="4b553-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4b553-138">System.Boolean</span></span>

## <span data-ttu-id="4b553-139">Note</span><span class="sxs-lookup"><span data-stu-id="4b553-139">NOTES</span></span>

## <span data-ttu-id="4b553-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4b553-140">RELATED LINKS</span></span>

[<span data-ttu-id="4b553-141">Get-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="4b553-141">Get-AzApiManagementOperation</span></span>](./Get-AzApiManagementOperation.md)

[<span data-ttu-id="4b553-142">New-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="4b553-142">New-AzApiManagementOperation</span></span>](./New-AzApiManagementOperation.md)

[<span data-ttu-id="4b553-143">Set-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="4b553-143">Set-AzApiManagementOperation</span></span>](./Set-AzApiManagementOperation.md)


