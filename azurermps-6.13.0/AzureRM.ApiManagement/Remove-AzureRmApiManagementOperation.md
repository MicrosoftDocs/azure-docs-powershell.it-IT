---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: A4A8D996-72A2-4154-98DA-5F84CAA010B9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementOperation.md
ms.openlocfilehash: 1a3fd2ca25099be029616e048c5ebfa0e398229e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507731"
---
# <span data-ttu-id="05027-101">Remove-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="05027-101">Remove-AzureRmApiManagementOperation</span></span>

## <span data-ttu-id="05027-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="05027-102">SYNOPSIS</span></span>
<span data-ttu-id="05027-103">Rimuove un'operazione esistente.</span><span class="sxs-lookup"><span data-stu-id="05027-103">Removes an existing operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="05027-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="05027-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -OperationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="05027-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="05027-105">DESCRIPTION</span></span>
<span data-ttu-id="05027-106">Il cmdlet **Remove-AzureRmApiManagementOperation** rimuove un'operazione esistente.</span><span class="sxs-lookup"><span data-stu-id="05027-106">The **Remove-AzureRmApiManagementOperation** cmdlet removes an existing operation.</span></span>

## <span data-ttu-id="05027-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="05027-107">EXAMPLES</span></span>

### <span data-ttu-id="05027-108">Esempio 1: rimuovere un'operazione API esistente</span><span class="sxs-lookup"><span data-stu-id="05027-108">Example 1: Remove an existing API Operation</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementOperation -Context $apimContext -ApiId "0123456789" -OperationId "9876543210" -Force
```

<span data-ttu-id="05027-109">Questo comando rimuove un'operazione API esistente.</span><span class="sxs-lookup"><span data-stu-id="05027-109">This command removes an existing API Operation.</span></span>

## <span data-ttu-id="05027-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="05027-110">PARAMETERS</span></span>

### <span data-ttu-id="05027-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="05027-111">-ApiId</span></span>
<span data-ttu-id="05027-112">Specifica l'identificatore dell'API.</span><span class="sxs-lookup"><span data-stu-id="05027-112">Specifies the identifier of the API.</span></span>

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

### <span data-ttu-id="05027-113">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="05027-113">-ApiRevision</span></span>
<span data-ttu-id="05027-114">Identificatore della revisione API.</span><span class="sxs-lookup"><span data-stu-id="05027-114">Identifier of API Revision.</span></span> <span data-ttu-id="05027-115">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="05027-115">This parameter is optional.</span></span> <span data-ttu-id="05027-116">Se non specificato, l'operazione verrà rimossa dalla revisione API attualmente attiva.</span><span class="sxs-lookup"><span data-stu-id="05027-116">If not specified, the operation will be removed from the currently active api revision.</span></span>

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

### <span data-ttu-id="05027-117">-Contesto</span><span class="sxs-lookup"><span data-stu-id="05027-117">-Context</span></span>
<span data-ttu-id="05027-118">Specifica un'istanza di **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="05027-118">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="05027-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05027-119">-DefaultProfile</span></span>
<span data-ttu-id="05027-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="05027-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="05027-121">-OperationId</span><span class="sxs-lookup"><span data-stu-id="05027-121">-OperationId</span></span>
<span data-ttu-id="05027-122">Specifica l'identificatore dell'operazione API.</span><span class="sxs-lookup"><span data-stu-id="05027-122">Specifies the identifier of the API operation.</span></span>

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

### <span data-ttu-id="05027-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="05027-123">-PassThru</span></span>
<span data-ttu-id="05027-124">Indica che questo cmdlet restituisce un valore di $True se ha esito positivo oppure un valore di $False, in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="05027-124">Indicates that this cmdlet returns a value of $True if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="05027-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="05027-125">-Confirm</span></span>
<span data-ttu-id="05027-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05027-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05027-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05027-127">-WhatIf</span></span>
<span data-ttu-id="05027-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="05027-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05027-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="05027-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05027-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05027-130">CommonParameters</span></span>
<span data-ttu-id="05027-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05027-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05027-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05027-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05027-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="05027-133">INPUTS</span></span>

### <span data-ttu-id="05027-134">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="05027-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="05027-135">System. String</span><span class="sxs-lookup"><span data-stu-id="05027-135">System.String</span></span>

### <span data-ttu-id="05027-136">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="05027-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="05027-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="05027-137">OUTPUTS</span></span>

### <span data-ttu-id="05027-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="05027-138">System.Boolean</span></span>

## <span data-ttu-id="05027-139">Note</span><span class="sxs-lookup"><span data-stu-id="05027-139">NOTES</span></span>

## <span data-ttu-id="05027-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="05027-140">RELATED LINKS</span></span>

[<span data-ttu-id="05027-141">Get-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="05027-141">Get-AzureRmApiManagementOperation</span></span>](./Get-AzureRmApiManagementOperation.md)

[<span data-ttu-id="05027-142">New-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="05027-142">New-AzureRmApiManagementOperation</span></span>](./New-AzureRmApiManagementOperation.md)

[<span data-ttu-id="05027-143">Set-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="05027-143">Set-AzureRmApiManagementOperation</span></span>](./Set-AzureRmApiManagementOperation.md)


