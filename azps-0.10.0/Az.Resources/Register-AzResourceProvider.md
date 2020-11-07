---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D5067FD8-2FB1-413C-9F59-84E83A74343E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/register-Azresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Register-AzResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Register-AzResourceProvider.md
ms.openlocfilehash: 7f9a5089e48da7c49716abe2bdbe710c0cf30e3b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93862453"
---
# <span data-ttu-id="5dd25-101">Register-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="5dd25-101">Register-AzResourceProvider</span></span>

## <span data-ttu-id="5dd25-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5dd25-102">SYNOPSIS</span></span>
<span data-ttu-id="5dd25-103">Registra un provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="5dd25-103">Registers a resource provider.</span></span>

## <span data-ttu-id="5dd25-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5dd25-104">SYNTAX</span></span>

```
Register-AzResourceProvider -ProviderNamespace <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5dd25-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5dd25-105">DESCRIPTION</span></span>
<span data-ttu-id="5dd25-106">Il cmdlet **Register-AzResourceProvider** registra un provider di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="5dd25-106">The **Register-AzResourceProvider** cmdlet registers an Azure resource provider.</span></span>

## <span data-ttu-id="5dd25-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5dd25-107">EXAMPLES</span></span>

### <span data-ttu-id="5dd25-108">Esempio 1: registrare un provider</span><span class="sxs-lookup"><span data-stu-id="5dd25-108">Example 1: Register a provider</span></span>
```
PS C:\>Register-AzResourceProvider -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="5dd25-109">Questo registra il provider Microsoft. Network per l'account.</span><span class="sxs-lookup"><span data-stu-id="5dd25-109">This registers the Microsoft.Network provider for your account.</span></span>

## <span data-ttu-id="5dd25-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5dd25-110">PARAMETERS</span></span>

### <span data-ttu-id="5dd25-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="5dd25-111">-ApiVersion</span></span>
<span data-ttu-id="5dd25-112">Specifica la versione dell'API supportata dal provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="5dd25-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="5dd25-113">Puoi specificare una versione diversa rispetto alla versione predefinita.</span><span class="sxs-lookup"><span data-stu-id="5dd25-113">You can specify a different version than the default version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dd25-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5dd25-114">-DefaultProfile</span></span>
<span data-ttu-id="5dd25-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="5dd25-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dd25-116">-Pre</span><span class="sxs-lookup"><span data-stu-id="5dd25-116">-Pre</span></span>
<span data-ttu-id="5dd25-117">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="5dd25-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dd25-118">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="5dd25-118">-ProviderNamespace</span></span>
<span data-ttu-id="5dd25-119">Specifica lo spazio dei nomi del provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="5dd25-119">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="5dd25-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5dd25-120">-Confirm</span></span>
<span data-ttu-id="5dd25-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5dd25-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5dd25-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5dd25-122">-WhatIf</span></span>
<span data-ttu-id="5dd25-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5dd25-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5dd25-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5dd25-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5dd25-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5dd25-125">CommonParameters</span></span>
<span data-ttu-id="5dd25-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5dd25-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5dd25-127">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5dd25-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5dd25-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5dd25-128">INPUTS</span></span>

## <span data-ttu-id="5dd25-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5dd25-129">OUTPUTS</span></span>

## <span data-ttu-id="5dd25-130">Note</span><span class="sxs-lookup"><span data-stu-id="5dd25-130">NOTES</span></span>

## <span data-ttu-id="5dd25-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5dd25-131">RELATED LINKS</span></span>

[<span data-ttu-id="5dd25-132">Get-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="5dd25-132">Get-AzResourceProvider</span></span>](./Get-AzResourceProvider.md)

[<span data-ttu-id="5dd25-133">Annullamento della registrazione-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="5dd25-133">Unregister-AzResourceProvider</span></span>](./Unregister-AzResourceProvider.md)


