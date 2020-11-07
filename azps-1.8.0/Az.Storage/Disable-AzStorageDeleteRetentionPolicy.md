---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/disable-azstoragedeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageDeleteRetentionPolicy.md
ms.openlocfilehash: fad4e01b06182d689e105f4b5e6c6a580e1b20b6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676658"
---
# <span data-ttu-id="c8add-101">Disable-AzStorageDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="c8add-101">Disable-AzStorageDeleteRetentionPolicy</span></span>

## <span data-ttu-id="c8add-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c8add-102">SYNOPSIS</span></span>
<span data-ttu-id="c8add-103">Disabilitare i criteri di conservazione Elimina per il servizio BLOB di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="c8add-103">Disable delete retention policy  for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="c8add-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c8add-104">SYNTAX</span></span>

```
Disable-AzStorageDeleteRetentionPolicy [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8add-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c8add-105">DESCRIPTION</span></span>
<span data-ttu-id="c8add-106">Il cmdlet **Disable-AzStorageDeleteRetentionPolicy Disabilita** l'eliminazione dei criteri di conservazione per il servizio BLOB di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="c8add-106">The **Disable-AzStorageDeleteRetentionPolicy** cmdlet disables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="c8add-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c8add-107">EXAMPLES</span></span>

### <span data-ttu-id="c8add-108">Esempio 1: disabilitare l'eliminazione dei criteri di conservazione per il servizio BLOB</span><span class="sxs-lookup"><span data-stu-id="c8add-108">Example 1: Disable delete retention policy for the Blob service</span></span>
```
C:\PS>Disable-AzStorageDeleteRetentionPolicy
```

<span data-ttu-id="c8add-109">Questo comando Disabilita l'eliminazione dei criteri di conservazione per il servizio BLOB.</span><span class="sxs-lookup"><span data-stu-id="c8add-109">This command disables delete retention policy for the Blob service.</span></span>

## <span data-ttu-id="c8add-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c8add-110">PARAMETERS</span></span>

### <span data-ttu-id="c8add-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="c8add-111">-Context</span></span>
<span data-ttu-id="c8add-112">Oggetto contesto di archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="c8add-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="c8add-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8add-113">-DefaultProfile</span></span>
<span data-ttu-id="c8add-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c8add-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8add-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c8add-115">-PassThru</span></span>
<span data-ttu-id="c8add-116">Visualizza DeleteRetentionPolicyProperties</span><span class="sxs-lookup"><span data-stu-id="c8add-116">Display DeleteRetentionPolicyProperties</span></span>

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

### <span data-ttu-id="c8add-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c8add-117">-Confirm</span></span>
<span data-ttu-id="c8add-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8add-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8add-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8add-119">-WhatIf</span></span>
<span data-ttu-id="c8add-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c8add-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8add-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c8add-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8add-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8add-122">CommonParameters</span></span>
<span data-ttu-id="c8add-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8add-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8add-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8add-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8add-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c8add-125">INPUTS</span></span>

### <span data-ttu-id="c8add-126">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="c8add-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="c8add-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c8add-127">OUTPUTS</span></span>

### <span data-ttu-id="c8add-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="c8add-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span></span>

## <span data-ttu-id="c8add-129">Note</span><span class="sxs-lookup"><span data-stu-id="c8add-129">NOTES</span></span>

## <span data-ttu-id="c8add-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c8add-130">RELATED LINKS</span></span>
