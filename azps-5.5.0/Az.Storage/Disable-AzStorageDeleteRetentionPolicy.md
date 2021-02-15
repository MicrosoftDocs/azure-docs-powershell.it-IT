---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/disable-azstoragedeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageDeleteRetentionPolicy.md
ms.openlocfilehash: c8a32cb86ace86cb0f2775db98f49f57408be6f4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190911"
---
# <span data-ttu-id="dc68e-101">Disable-AzStorageDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="dc68e-101">Disable-AzStorageDeleteRetentionPolicy</span></span>

## <span data-ttu-id="dc68e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc68e-102">SYNOPSIS</span></span>
<span data-ttu-id="dc68e-103">Disabilitare l'eliminazione dei criteri di conservazione per il servizio BLOB Archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="dc68e-103">Disable delete retention policy  for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="dc68e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dc68e-104">SYNTAX</span></span>

```
Disable-AzStorageDeleteRetentionPolicy [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc68e-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="dc68e-105">DESCRIPTION</span></span>
<span data-ttu-id="dc68e-106">Il cmdlet **Disable-AzStorageDeleteRetentionPolicy** disabilita l'eliminazione dei criteri di conservazione per il servizio BLOB di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="dc68e-106">The **Disable-AzStorageDeleteRetentionPolicy** cmdlet disables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="dc68e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dc68e-107">EXAMPLES</span></span>

### <span data-ttu-id="dc68e-108">Esempio 1: Disabilitare l'eliminazione dei criteri di conservazione per il servizio BLOB</span><span class="sxs-lookup"><span data-stu-id="dc68e-108">Example 1: Disable delete retention policy for the Blob service</span></span>
```
C:\PS>Disable-AzStorageDeleteRetentionPolicy
```

<span data-ttu-id="dc68e-109">Questo comando disabilita l'eliminazione dei criteri di conservazione per il servizio BLOB.</span><span class="sxs-lookup"><span data-stu-id="dc68e-109">This command disables delete retention policy for the Blob service.</span></span>

## <span data-ttu-id="dc68e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dc68e-110">PARAMETERS</span></span>

### <span data-ttu-id="dc68e-111">-Context</span><span class="sxs-lookup"><span data-stu-id="dc68e-111">-Context</span></span>
<span data-ttu-id="dc68e-112">Oggetto contesto archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="dc68e-112">Azure Storage Context Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dc68e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc68e-113">-DefaultProfile</span></span>
<span data-ttu-id="dc68e-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dc68e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc68e-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dc68e-115">-PassThru</span></span>
<span data-ttu-id="dc68e-116">Display DeleteRetentionPolicyProperties</span><span class="sxs-lookup"><span data-stu-id="dc68e-116">Display DeleteRetentionPolicyProperties</span></span>

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

### <span data-ttu-id="dc68e-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dc68e-117">-Confirm</span></span>
<span data-ttu-id="dc68e-118">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc68e-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc68e-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc68e-119">-WhatIf</span></span>
<span data-ttu-id="dc68e-120">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dc68e-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc68e-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dc68e-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc68e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc68e-122">CommonParameters</span></span>
<span data-ttu-id="dc68e-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc68e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc68e-124">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc68e-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc68e-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="dc68e-125">INPUTS</span></span>

### <span data-ttu-id="dc68e-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="dc68e-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="dc68e-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dc68e-127">OUTPUTS</span></span>

### <span data-ttu-id="dc68e-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="dc68e-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span></span>

## <span data-ttu-id="dc68e-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="dc68e-129">NOTES</span></span>

## <span data-ttu-id="dc68e-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dc68e-130">RELATED LINKS</span></span>
